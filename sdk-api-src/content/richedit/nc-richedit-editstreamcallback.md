---
UID: NC:richedit.EDITSTREAMCALLBACK
title: EDITSTREAMCALLBACK
author: windows-sdk-content
description: The EditStreamCallback function is an application defined callback function used with the EM_STREAMIN and EM_STREAMOUT messages.
old-location: controls\EditStreamCallback.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditcallbackfunctions\editstreamcallback.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: EditStreamCallback, EditStreamCallback callback, EditStreamCallback callback function [Windows Controls], _win32_EditStreamCallback, _win32_EditStreamCallback_cpp, controls.EditStreamCallback, controls._win32_EditStreamCallback, richedit/EditStreamCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: RM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Richedit.h
api_name:
 - EditStreamCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# EDITSTREAMCALLBACK callback function


## -description


The <i>EditStreamCallback</i> function is an application defined callback function used with the <a href="https://msdn.microsoft.com/b8d3a108-b415-4f5e-99e7-0e0e7a82a778">EM_STREAMIN</a> and <a href="https://msdn.microsoft.com/3f14aaac-4b17-47af-8f2b-503390631a88">EM_STREAMOUT</a> messages. It is used to transfer a stream of data into or out of a rich edit control. The 
			<b>EDITSTREAMCALLBACK</b> type defines a pointer to this callback function. <i>EditStreamCallback</i> is a placeholder for the application-defined function name. 


## -parameters




### -param dwCookie [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD_PTR</a></b>

Value of the 
					<i>dwCookie</i> member of the <a href="https://msdn.microsoft.com/613c29f5-6ae6-476f-bb5e-fdddab731d9c">EDITSTREAM</a> structure. The application specifies this value when it sends the <a href="https://msdn.microsoft.com/b8d3a108-b415-4f5e-99e7-0e0e7a82a778">EM_STREAMIN</a> or <a href="https://msdn.microsoft.com/3f14aaac-4b17-47af-8f2b-503390631a88">EM_STREAMOUT</a> message. 


### -param pbBuff [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPBYTE</a></b>

Pointer to a buffer to read from or write to. For a stream-in (read) operation, the callback function fills this buffer with data to transfer into the rich edit control. For a stream-out (write) operation, the buffer contains data from the control that the callback function writes to some storage. 


### -param cb [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Number of bytes to read or write. 


### -param *pcb [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

Pointer to a variable that the callback function sets to the number of bytes actually read or written. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The callback function returns zero to indicate success.

The callback function returns a nonzero value to indicate an error. If an error occurs, the read or write operation ends and the rich edit control discards any data in the 
						<i>pbBuff</i> buffer. If the callback function returns a nonzero value, the rich edit control uses the 
						<i>dwError</i> member of the <a href="https://msdn.microsoft.com/613c29f5-6ae6-476f-bb5e-fdddab731d9c">EDITSTREAM</a> structure to pass the value back to the application.




## -remarks



When you send the <a href="https://msdn.microsoft.com/b8d3a108-b415-4f5e-99e7-0e0e7a82a778">EM_STREAMIN</a> or <a href="https://msdn.microsoft.com/3f14aaac-4b17-47af-8f2b-503390631a88">EM_STREAMOUT</a> message to a rich edit control, the 
				<i>pfnCallback</i> member of the <a href="https://msdn.microsoft.com/613c29f5-6ae6-476f-bb5e-fdddab731d9c">EDITSTREAM</a> structure specifies a pointer to an <i>EditStreamCallback</i> function. The rich edit control repeatedly calls the function to transfer a stream of data into or out of the control. 

When you send the <a href="https://msdn.microsoft.com/b8d3a108-b415-4f5e-99e7-0e0e7a82a778">EM_STREAMIN</a> or <a href="https://msdn.microsoft.com/3f14aaac-4b17-47af-8f2b-503390631a88">EM_STREAMOUT</a> message, you specify a value for the 
				<i>dwCookie</i> member of the <a href="https://msdn.microsoft.com/613c29f5-6ae6-476f-bb5e-fdddab731d9c">EDITSTREAM</a> structure. The rich edit control uses the 
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




<a href="https://msdn.microsoft.com/613c29f5-6ae6-476f-bb5e-fdddab731d9c">EDITSTREAM</a>



<a href="https://msdn.microsoft.com/b8d3a108-b415-4f5e-99e7-0e0e7a82a778">EM_STREAMIN</a>



<a href="https://msdn.microsoft.com/3f14aaac-4b17-47af-8f2b-503390631a88">EM_STREAMOUT</a>



<b>Reference</b>
 

 

