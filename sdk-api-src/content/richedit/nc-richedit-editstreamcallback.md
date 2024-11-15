---
UID: NC:richedit.EDITSTREAMCALLBACK
title: EDITSTREAMCALLBACK (richedit.h)
description: The EditStreamCallback function is an application defined callback function used with the EM_STREAMIN and EM_STREAMOUT messages.
helpviewer_keywords: ["EditStreamCallback","EditStreamCallback callback","EditStreamCallback callback function [Windows Controls]","_win32_EditStreamCallback","_win32_EditStreamCallback_cpp","controls.EditStreamCallback","controls._win32_EditStreamCallback","richedit/EditStreamCallback"]
old-location: controls\EditStreamCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditcallbackfunctions\editstreamcallback.htm
ms.date: 12/05/2018
ms.keywords: EditStreamCallback, EditStreamCallback callback, EditStreamCallback callback function [Windows Controls], _win32_EditStreamCallback, _win32_EditStreamCallback_cpp, controls.EditStreamCallback, controls._win32_EditStreamCallback, richedit/EditStreamCallback
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EDITSTREAMCALLBACK
 - richedit/EDITSTREAMCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Richedit.h
api_name:
 - EditStreamCallback
---

# EDITSTREAMCALLBACK callback function


## -description

The <i>EditStreamCallback</i> function is an application defined callback function used with the <a href="/windows/win32/controls/em-streamin">EM_STREAMIN</a> and <a href="/windows/win32/controls/em-streamout">EM_STREAMOUT</a> messages. It is used to transfer a stream of data into or out of a rich edit control. The 
			<b>EDITSTREAMCALLBACK</b> type defines a pointer to this callback function. <i>EditStreamCallback</i> is a placeholder for the application-defined function name.

## -parameters

### -param dwCookie [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

Value of the 
					<i>dwCookie</i> member of the <a href="/windows/win32/api/richedit/ns-richedit-editstream">EDITSTREAM</a> structure. The application specifies this value when it sends the <a href="/windows/win32/controls/em-streamin">EM_STREAMIN</a> or <a href="/windows/win32/controls/em-streamout">EM_STREAMOUT</a> message.

### -param pbBuff [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPBYTE</a></b>

Pointer to a buffer to read from or write to. For a stream-in (read) operation, the callback function fills this buffer with data to transfer into the rich edit control. For a stream-out (write) operation, the buffer contains data from the control that the callback function writes to some storage.

### -param cb [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Number of bytes to read or write.

### -param pcb [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

Pointer to a variable that the callback function sets to the number of bytes actually read or written.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The callback function returns zero to indicate success.

The callback function returns a nonzero value to indicate an error. If an error occurs, the read or write operation ends and the rich edit control discards any data in the 
						<i>pbBuff</i> buffer. If the callback function returns a nonzero value, the rich edit control uses the 
						<i>dwError</i> member of the <a href="/windows/win32/api/richedit/ns-richedit-editstream">EDITSTREAM</a> structure to pass the value back to the application.

## -remarks

When you send the <a href="/windows/win32/controls/em-streamin">EM_STREAMIN</a> or <a href="/windows/win32/controls/em-streamout">EM_STREAMOUT</a> message to a rich edit control, the 
				<i>pfnCallback</i> member of the <a href="/windows/win32/api/richedit/ns-richedit-editstream">EDITSTREAM</a> structure specifies a pointer to an <i>EditStreamCallback</i> function. The rich edit control repeatedly calls the function to transfer a stream of data into or out of the control. 

When you send the <a href="/windows/win32/controls/em-streamin">EM_STREAMIN</a> or <a href="/windows/win32/controls/em-streamout">EM_STREAMOUT</a> message, you specify a value for the 
				<i>dwCookie</i> member of the <a href="/windows/win32/api/richedit/ns-richedit-editstream">EDITSTREAM</a> structure. The rich edit control uses the 
				<i>dwCookie</i> parameter to pass this value to your <i>EditStreamCallback</i> function. For example, you might use 
				<i>dwCookie</i> to pass a handle to an open file. The callback function can then use the 
				<i>dwCookie</i> handle to read from or write to the file. 

The control calls the callback function repeatedly, transferring a portion of the data with each call. The control continues to call the callback function until one of the following conditions occurs: 

<ul>
<li>The callback function returns a nonzero value. </li>
<li>The callback function returns zero in the *
						<i>pcb</i> parameter. </li>
<li>An error occurs that prevents the rich edit control from transferring data into or out of itself. Examples are out-of-memory situations, failure of a system function, or an invalid character in the read buffer. </li>
<li>For a stream-in operation, the RTF code contains data specifying the end of an RTF block. </li>
<li>For a stream-in operation on a single-line edit control, the callback reads in an end-of-paragraph character (CR, LF, VT, LS, or PS). </li>
</ul>

## -see-also

<a href="/windows/win32/api/richedit/ns-richedit-editstream">EDITSTREAM</a>



<a href="/windows/win32/controls/em-streamin">EM_STREAMIN</a>



<a href="/windows/win32/controls/em-streamout">EM_STREAMOUT</a>



<b>Reference</b>
