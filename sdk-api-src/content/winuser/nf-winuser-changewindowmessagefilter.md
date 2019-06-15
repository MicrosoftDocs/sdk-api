---
UID: NF:winuser.ChangeWindowMessageFilter
title: ChangeWindowMessageFilter function (winuser.h)
author: windows-sdk-content
description: Adds or removes a message from the User Interface Privilege Isolation (UIPI) message filter.
old-location: winmsg\changewindowmessagefilter.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\changewindowmessagefilter.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ChangeWindowMessageFilter, ChangeWindowMessageFilter function [Windows and Messages], MSGFLT_ADD, MSGFLT_REMOVE, _win32_ChangeWindowMessageFilter, _win32_changewindowmessagefilter_cpp, winmsg.changewindowmessagefilter, winui._win32_changewindowmessagefilter, winuser/ChangeWindowMessageFilter
ms.topic: function
f1_keywords: ["winuser/ChangeWindowMessageFilter"]
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - ChangeWindowMessageFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ChangeWindowMessageFilter function


## -description


<p class="CCE_Message">[Using the 
		<b>ChangeWindowMessageFilter</b> function is not recommended, as it has process-wide scope. 
		Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-changewindowmessagefilterex">ChangeWindowMessageFilterEx</a> function to 
		control access to specific windows as needed.
		<b>ChangeWindowMessageFilter</b> may not be supported in future versions of Windows.]

Adds or removes a message from the User Interface Privilege Isolation (UIPI) message filter.


## -parameters




### -param message [in]

Type: <b>UINT</b>

The message to add to or remove from the filter.


### -param dwFlag [in]

Type: <b>DWORD</b>

The action to be performed. One of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSGFLT_ADD"></a><a id="msgflt_add"></a><dl>
<dt><b>MSGFLT_ADD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Adds the <i>message</i> to the filter. This has the effect of allowing the message to be received.

</td>
</tr>
<tr>
<td width="40%"><a id="MSGFLT_REMOVE"></a><a id="msgflt_remove"></a><dl>
<dt><b>MSGFLT_REMOVE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Removes the <i>message</i> from the filter. This has the effect of blocking the message.

</td>
</tr>
</table>
 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

                    

<div class="alert"><b>Note</b>  A message can be successfully removed from the filter, but that is not a guarantee that the message will be blocked. See the Remarks section for more details.</div>
<div> </div>



## -remarks



UIPI is a security feature that prevents messages from being received from a lower integrity level sender. All such messages with a value above <b>WM_USER</b> are blocked by default. The filter, somewhat contrary to intuition, is a list of messages that are allowed through. Therefore, adding a message to the filter allows that message to be received from a lower integrity sender, while removing a message blocks that message from being received.

Certain messages with a value less than <b>WM_USER</b> are required to pass through the filter regardless of the filter setting. You can call this function to remove one of those messages from the filter and it will return <b>TRUE</b>. However, the message will still be received by the calling process.

Processes at or below <b>SECURITY_MANDATORY_LOW_RID</b> are not allowed to change the filter. If those processes call this function, it will fail.

For more information on integrity levels, see <a href="http://go.microsoft.com/fwlink/p/?linkid=204861">Understanding and Working in Protected Mode Internet Explorer</a>.



