.. This file is licensed under the MIT License (MIT) available on
   http://opensource.org/licenses/MIT.

listlabels
==========

``listlabels ( "purpose" )``

Returns the list of all labels, or labels that are assigned to addresses with a specific purpose.

Argument #1 - purpose
~~~~~~~~~~~~~~~~~~~~~

**Type:** string, optional

Address purpose to list labels for ('send','receive'). An empty string is the same as not providing this argument.

Result
~~~~~~

::

  [           (json array)
    "str",    (string) Label name
    ...
  ]

Examples
~~~~~~~~


.. highlight:: shell

List all labels::

  digibyte-cli listlabels

List labels that have receiving addresses::

  digibyte-cli listlabels receive

List labels that have sending addresses::

  digibyte-cli listlabels send

As a JSON-RPC call::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "listlabels", "params": [receive]}' -H 'content-type: text/plain;' http://127.0.0.1:14022/

