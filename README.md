NAME
    CGI::Application::Plugin::RemoteIP - Unified Remote IP handling

SYNOPSIS
      use CGI::Application::Plugin::RemoteIP;


      # Your application
      sub run_mode {
        my ($self) = ( @_);

        my $ip = $self->remote_ip();
      }

DESCRIPTION
    This module simplifies the handling of the detection of the remote IP
    address(es) of visitors.

MOTIVATION
    This module allows you to remove scattered references in your code, such
    as:

        my $ip = $ENV{'REMOTE_ADDR'};
        $ip =~ s/^::ffff://g;
        ..

    Instead your code and use the simpler expression:

        my $ip = $self->remote_ip();

METHODS
  import
    Force the "remote_ip" method into the caller's namespace.

  remote_ip
    Return the remote IP of the visitor

AUTHOR
    Steve Kemp <steve@steve.org.uk>

COPYRIGHT AND LICENSE
    Copyright (C) 2015 Steve Kemp <steve@steve.org.uk>.

    This library is free software. You can modify and or distribute it under
    the same terms as Perl itself.

