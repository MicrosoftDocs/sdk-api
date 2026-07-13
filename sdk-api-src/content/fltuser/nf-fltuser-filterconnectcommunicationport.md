---
UID: NF:fltuser.FilterConnectCommunicationPort
title: FilterConnectCommunicationPort function (fltuser.h)
description: FilterConnectCommunicationPort opens a new connection to a communication server port that is created by a file system minifilter.
helpviewer_keywords: ["FLT_PORT_FLAG_SYNC_HANDLE","FilterConnectCommunicationPort","FilterConnectCommunicationPort function [Installable File System Drivers]","FltWin32ApiRef_3459349f-ecfb-47c0-ae70-3f75e1d18435.xml","fltuser/FilterConnectCommunicationPort","ifsk.filterconnectcommunicationport"]
old-location: ifsk\filterconnectcommunicationport.htm
tech.root: ifsk
ms.assetid: 294783f2-2cbf-4eea-82ae-a396c62f911a
ms.date: 12/05/2018
ms.keywords: FLT_PORT_FLAG_SYNC_HANDLE, FilterConnectCommunicationPort, FilterConnectCommunicationPort function [Installable File System Drivers], FltWin32ApiRef_3459349f-ecfb-47c0-ae70-3f75e1d18435.xml, fltuser/FilterConnectCommunicationPort, ifsk.filterconnectcommunicationport
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterConnectCommunicationPort
 - fltuser/FilterConnectCommunicationPort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterConnectCommunicationPort
---

# FilterConnectCommunicationPort function


## -description

<b>FilterConnectCommunicationPort</b> opens a new connection to a communication server port that is created by a file system minifilter.

## -parameters

### -param lpPortName [in]

Pointer to a NULL-terminated wide-character string containing the fully qualified name of the communication server port (for example, L"\\MyFilterPort").

### -param dwOptions [in]

Connection options for the communication port. Prior to Windows 8.1, this value is set to 0.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FLT_PORT_FLAG_SYNC_HANDLE"></a><a id="flt_port_flag_sync_handle"></a><dl>
<dt><b>FLT_PORT_FLAG_SYNC_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle returned in <i>hPort</i> is for synchronous I/O. This flag is available starting with Windows 8.1.

</td>
</tr>
</table>

### -param lpContext [in, optional]

Pointer to caller-supplied context information to be passed to the kernel-mode minifilter's connect notification routine. (See the <i>ConnectNotifyCallback</i> parameter in the reference page for <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcreatecommunicationport">FltCreateCommunicationPort</a>.) This parameter is optional and can be <b>NULL</b>.

### -param wSizeOfContext [in]

Size, in bytes, of the structure that the <i>lpContext</i> parameter points to. If the value of <i>lpContext</i> is non-<b>NULL</b>, this parameter must be nonzero. If <i>lpContext</i> is <b>NULL</b>, this parameter must be zero.

### -param lpSecurityAttributes [in, optional]

Pointer to a SECURITY_ATTRIBUTES structure that determines whether the returned handle can be inherited by child processes. For more information about the SECURITY_ATTRIBUTES structure, see the Microsoft Windows SDK documentation. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the handle cannot be inherited.

### -param hPort [out]

Pointer to a caller-allocated variable that receives a handle for the newly created connection port if the call to <b>FilterConnectCommunicationPort</b> succeeds; otherwise, it receives INVALID_HANDLE_VALUE.

## -returns

<b>FilterConnectCommunicationPort</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

<b>FilterConnectCommunicationPort</b> opens a connection to a minifilter's communication server port on behalf of a user-mode application. The application uses the resulting connection port handle to communicate with the minifilter. 

After it successfully calls <b>FilterConnectCommunicationPort</b>, the application can send messages to the minifilter through the connection port by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filtersendmessage">FilterSendMessage</a>. It can also receive and reply to messages from the minifilter by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filtergetmessage">FilterGetMessage</a> and <a href="/windows/desktop/api/fltuser/nf-fltuser-filterreplymessage">FilterReplyMessage</a>, respectively. The connection port handle returned in the <i>hPort</i> parameter is passed as the first parameter to <b>FilterSendMessage</b>, <b>FilterGetMessage</b>, and <b>FilterReplyMessage</b>. 

Any handle that is obtained from <b>FilterConnectCommunicationPort</b> must eventually be released by calling <a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

## -see-also

<a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtergetmessage">FilterGetMessage</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterreplymessage">FilterReplyMessage</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtersendmessage">FilterSendMessage</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltbuilddefaultsecuritydescriptor">FltBuildDefaultSecurityDescriptor</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcloseclientport">FltCloseClientPort</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltclosecommunicationport">FltCloseCommunicationPort</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcreatecommunicationport">FltCreateCommunicationPort</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltfreesecuritydescriptor">FltFreeSecurityDescriptor</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>