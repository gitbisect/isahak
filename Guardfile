
def on_rb_or_yml_update
  rubocop_auto_correct = 'rubocop -a'
  run_rspec = 'rspec spec'

  command_to_run = "#{rubocop_auto_correct}; #{run_rspec};"
  command_to_run
end

guard :shell do
  watch(/(.*)\.rb$/) { |_m| `#{on_rb_or_yml_update}` }
  watch(/(.*)\.erb$/) { |_m| `#{on_rb_or_yml_update}` }
  watch(/(.*)\.yml$/) { |_m| `#{on_rb_or_yml_update}` }
end
