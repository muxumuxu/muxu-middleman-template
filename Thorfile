require 'thor/group'

module Middleman
  class Generator < ::Thor::Group
    include ::Thor::Actions

    source_root File.expand_path(File.dirname(__FILE__))

    def copy_default_files
      directory 'template', '.', exclude_pattern: /\.DS_Store$/
    end

    def git_setup
	    git :init
		  git add: "."
		  git commit: %Q{ -m "Initial Middleman app" }
    end
  end
end
