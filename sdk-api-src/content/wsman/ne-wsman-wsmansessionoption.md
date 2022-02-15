---
UID: NE:wsman.WSManSessionOption
title: WSManSessionOption (wsman.h)
description: Defines a set of extended options for the session. These options are used with the WSManSetSessionOption method.
helpviewer_keywords: ["WSMAN_OPTION_ALLOW_NEGOTIATE_IMPLICIT_CREDENTIALS","WSMAN_OPTION_DEFAULT_OPERATION_TIMEOUTMS","WSMAN_OPTION_ENABLE_SPN_SERVER_PORT","WSMAN_OPTION_LOCALE","WSMAN_OPTION_MACHINE_ID","WSMAN_OPTION_MAX_ENVELOPE_SIZE_KB","WSMAN_OPTION_REDIRECT_LOCATION","WSMAN_OPTION_SHELL_MAX_DATA_SIZE_PER_MESSAGE_KB","WSMAN_OPTION_SKIP_CA_CHECK","WSMAN_OPTION_SKIP_CN_CHECK","WSMAN_OPTION_SKIP_REVOCATION_CHECK","WSMAN_OPTION_TIMEOUTMS_CLOSE_SHELL","WSMAN_OPTION_TIMEOUTMS_CREATE_SHELL","WSMAN_OPTION_TIMEOUTMS_RECEIVE_SHELL_OUTPUT","WSMAN_OPTION_TIMEOUTMS_RUN_SHELL_COMMAND","WSMAN_OPTION_TIMEOUTMS_SEND_SHELL_INPUT","WSMAN_OPTION_TIMEOUTMS_SIGNAL_SHELL","WSMAN_OPTION_UI_LANGUAGE","WSMAN_OPTION_UNENCRYPTED_MESSAGES","WSMAN_OPTION_UTF16","WSManSessionOption","WSManSessionOption enumeration [Windows Remote Management]","winrm.wsmansessionoption","wsman/WSMAN_OPTION_ALLOW_NEGOTIATE_IMPLICIT_CREDENTIALS","wsman/WSMAN_OPTION_DEFAULT_OPERATION_TIMEOUTMS","wsman/WSMAN_OPTION_ENABLE_SPN_SERVER_PORT","wsman/WSMAN_OPTION_LOCALE","wsman/WSMAN_OPTION_MACHINE_ID","wsman/WSMAN_OPTION_MAX_ENVELOPE_SIZE_KB","wsman/WSMAN_OPTION_REDIRECT_LOCATION","wsman/WSMAN_OPTION_SHELL_MAX_DATA_SIZE_PER_MESSAGE_KB","wsman/WSMAN_OPTION_SKIP_CA_CHECK","wsman/WSMAN_OPTION_SKIP_CN_CHECK","wsman/WSMAN_OPTION_SKIP_REVOCATION_CHECK","wsman/WSMAN_OPTION_TIMEOUTMS_CLOSE_SHELL","wsman/WSMAN_OPTION_TIMEOUTMS_CREATE_SHELL","wsman/WSMAN_OPTION_TIMEOUTMS_RECEIVE_SHELL_OUTPUT","wsman/WSMAN_OPTION_TIMEOUTMS_RUN_SHELL_COMMAND","wsman/WSMAN_OPTION_TIMEOUTMS_SEND_SHELL_INPUT","wsman/WSMAN_OPTION_TIMEOUTMS_SIGNAL_SHELL","wsman/WSMAN_OPTION_UI_LANGUAGE","wsman/WSMAN_OPTION_UNENCRYPTED_MESSAGES","wsman/WSMAN_OPTION_UTF16","wsman/WSManSessionOption"]
old-location: winrm\wsmansessionoption.htm
tech.root: winrm
ms.assetid: 6bfe6936-a9d2-4884-a354-41bd62a2feb0
ms.date: 12/05/2018
ms.keywords: WSMAN_OPTION_ALLOW_NEGOTIATE_IMPLICIT_CREDENTIALS, WSMAN_OPTION_DEFAULT_OPERATION_TIMEOUTMS, WSMAN_OPTION_ENABLE_SPN_SERVER_PORT, WSMAN_OPTION_LOCALE, WSMAN_OPTION_MACHINE_ID, WSMAN_OPTION_MAX_ENVELOPE_SIZE_KB, WSMAN_OPTION_REDIRECT_LOCATION, WSMAN_OPTION_SHELL_MAX_DATA_SIZE_PER_MESSAGE_KB, WSMAN_OPTION_SKIP_CA_CHECK, WSMAN_OPTION_SKIP_CN_CHECK, WSMAN_OPTION_SKIP_REVOCATION_CHECK, WSMAN_OPTION_TIMEOUTMS_CLOSE_SHELL, WSMAN_OPTION_TIMEOUTMS_CREATE_SHELL, WSMAN_OPTION_TIMEOUTMS_RECEIVE_SHELL_OUTPUT, WSMAN_OPTION_TIMEOUTMS_RUN_SHELL_COMMAND, WSMAN_OPTION_TIMEOUTMS_SEND_SHELL_INPUT, WSMAN_OPTION_TIMEOUTMS_SIGNAL_SHELL, WSMAN_OPTION_UI_LANGUAGE, WSMAN_OPTION_UNENCRYPTED_MESSAGES, WSMAN_OPTION_UTF16, WSManSessionOption, WSManSessionOption enumeration [Windows Remote Management], winrm.wsmansessionoption, wsman/WSMAN_OPTION_ALLOW_NEGOTIATE_IMPLICIT_CREDENTIALS, wsman/WSMAN_OPTION_DEFAULT_OPERATION_TIMEOUTMS, wsman/WSMAN_OPTION_ENABLE_SPN_SERVER_PORT, wsman/WSMAN_OPTION_LOCALE, wsman/WSMAN_OPTION_MACHINE_ID, wsman/WSMAN_OPTION_MAX_ENVELOPE_SIZE_KB, wsman/WSMAN_OPTION_REDIRECT_LOCATION, wsman/WSMAN_OPTION_SHELL_MAX_DATA_SIZE_PER_MESSAGE_KB, wsman/WSMAN_OPTION_SKIP_CA_CHECK, wsman/WSMAN_OPTION_SKIP_CN_CHECK, wsman/WSMAN_OPTION_SKIP_REVOCATION_CHECK, wsman/WSMAN_OPTION_TIMEOUTMS_CLOSE_SHELL, wsman/WSMAN_OPTION_TIMEOUTMS_CREATE_SHELL, wsman/WSMAN_OPTION_TIMEOUTMS_RECEIVE_SHELL_OUTPUT, wsman/WSMAN_OPTION_TIMEOUTMS_RUN_SHELL_COMMAND, wsman/WSMAN_OPTION_TIMEOUTMS_SEND_SHELL_INPUT, wsman/WSMAN_OPTION_TIMEOUTMS_SIGNAL_SHELL, wsman/WSMAN_OPTION_UI_LANGUAGE, wsman/WSMAN_OPTION_UNENCRYPTED_MESSAGES, wsman/WSMAN_OPTION_UTF16, wsman/WSManSessionOption
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSManSessionOption
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManSessionOption
 - wsman/WSManSessionOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSManSessionOption
---

# WSManSessionOption enumeration


## -description

Defines a set of extended options for the session. These options are used with the <a href="/windows/desktop/api/wsman/nf-wsman-wsmansetsessionoption">WSManSetSessionOption</a> method.

## -enum-fields

### -field WSMAN_OPTION_DEFAULT_OPERATION_TIMEOUTMS:1

Default time-out in milliseconds that applies to all operations on the client side.

### -field WSMAN_OPTION_MAX_RETRY_TIME:11

### -field WSMAN_OPTION_TIMEOUTMS_CREATE_SHELL:12

Time-out in milliseconds for <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> operations.

### -field WSMAN_OPTION_TIMEOUTMS_RUN_SHELL_COMMAND:13

Time-out in milliseconds for <a href="/windows/desktop/api/wsman/nf-wsman-wsmanrunshellcommand">WSManRunShellCommand</a> operations.

### -field WSMAN_OPTION_TIMEOUTMS_RECEIVE_SHELL_OUTPUT:14

Time-out in milliseconds for <a href="/windows/desktop/api/wsman/nf-wsman-wsmanreceiveshelloutput">WSManReceiveShellOutput</a> operations.

### -field WSMAN_OPTION_TIMEOUTMS_SEND_SHELL_INPUT:15

Time-out in milliseconds for <a href="/windows/desktop/api/wsman/nf-wsman-wsmansendshellinput">WSManSendShellInput</a> operations.

### -field WSMAN_OPTION_TIMEOUTMS_SIGNAL_SHELL:16

Time-out in milliseconds for <a href="/windows/desktop/api/wsman/nf-wsman-wsmansignalshell">WSManSignalShell</a> and <a href="/windows/desktop/api/wsman/nf-wsman-wsmanclosecommand">WSManCloseCommand</a> operations.

### -field WSMAN_OPTION_TIMEOUTMS_CLOSE_SHELL:17

Time-out in milliseconds for <a href="/windows/desktop/api/wsman/nf-wsman-wsmancloseshell">WSManCloseShell</a> operations connection options.

### -field WSMAN_OPTION_SKIP_CA_CHECK:18

Set to 1 to not validate the CA on the server certificate. The default is 0.

### -field WSMAN_OPTION_SKIP_CN_CHECK:19

Set to 1 to not validate the CN on the server certificate. The default is 0.

### -field WSMAN_OPTION_UNENCRYPTED_MESSAGES:20

Set to 1 to not encrypt messages. The default is 0.

### -field WSMAN_OPTION_UTF16:21

Set to 1 to send all network packets for remote operations in UTF16. Default of 0 causes network packets to be sent in UTF8.

### -field WSMAN_OPTION_ENABLE_SPN_SERVER_PORT:22

Set to 1 when using Negotiate authentication and the  port number is included in the connection. Default is 0.

### -field WSMAN_OPTION_MACHINE_ID:23

Set to 1 to identify this machine to the server by including the MachineID. The default is 0.

### -field WSMAN_OPTION_LOCALE:25

The language locale options. For more information about the language locales, see the    RFC 3066 specification from the Internet Engineering Task Force at <a href="https://www.ietf.org/rfc/rfc3066.txt">http://www.ietf.org/rfc/rfc3066.txt</a>.

### -field WSMAN_OPTION_UI_LANGUAGE:26

The UI language options. The UI language options  are defined in RFC 3066 format.   For more information about the UI language options, see the    RFC 3066 specification from the Internet Engineering Task Force at <a href="https://www.ietf.org/rfc/rfc3066.txt">http://www.ietf.org/rfc/rfc3066.txt</a>.

### -field WSMAN_OPTION_MAX_ENVELOPE_SIZE_KB:28

The maximum Simple Object Access Protocol (SOAP) envelope size. The default is 150 KB.

### -field WSMAN_OPTION_SHELL_MAX_DATA_SIZE_PER_MESSAGE_KB:29

The maximum size of the data that is  provided by the client.

### -field WSMAN_OPTION_REDIRECT_LOCATION:30

The redirect location.

<div class="alert"><b>Note</b>  It is recommended that all redirection use Secure Sockets Layer (SSL) and that all applications validate the redirected URI before creating a new session.</div>
<div> </div>

### -field WSMAN_OPTION_SKIP_REVOCATION_CHECK:31

Set to 1 to not validate the revocation status on the server certificate. The default is 0.

### -field WSMAN_OPTION_ALLOW_NEGOTIATE_IMPLICIT_CREDENTIALS:32

Set to 1 to allow default credentials for Negotiate. The default is 0.

### -field WSMAN_OPTION_USE_SSL:33

### -field WSMAN_OPTION_USE_INTEARACTIVE_TOKEN:34        
