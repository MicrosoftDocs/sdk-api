---
UID: NS:richedit._editstream
title: "_editstream"
author: windows-driver-content
description: Contains information that an application passes to a rich edit control in a EM_STREAMIN or EM_STREAMOUT message. The rich edit control uses the information to transfer a stream of data into or out of the control.
old-location: controls\EDITSTREAM.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\editstream.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: EDITSTREAM, EDITSTREAM structure [Windows Controls], _editstream, _win32_EDITSTREAM_str, _win32_EDITSTREAM_str_cpp, controls.EDITSTREAM, controls._win32_EDITSTREAM_str, richedit/EDITSTREAM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: EDITSTREAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Richedit.h
api_name:
-	EDITSTREAM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _editstream structure


## -description



	 Contains information that an application passes to a rich edit control in a <a href="https://msdn.microsoft.com/b8d3a108-b415-4f5e-99e7-0e0e7a82a778">EM_STREAMIN</a> or <a href="https://msdn.microsoft.com/3f14aaac-4b17-47af-8f2b-503390631a88">EM_STREAMOUT</a> message. The rich edit control uses the information to transfer a stream of data into or out of the control. 


## -struct-fields




### -field dwCookie

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD_PTR</a></b>

Specifies an application-defined value that the rich edit control passes to the <a href="https://msdn.microsoft.com/9445b141-bd0f-4bf6-8986-fbfeab9e8999">EditStreamCallback</a> callback function specified by the <b>pfnCallback</b> member. 


### -field dwError

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Indicates the results of the stream-in (read) or stream-out (write) operation. A value of zero indicates no error. A nonzero value can be the return value of the <a href="https://msdn.microsoft.com/9445b141-bd0f-4bf6-8986-fbfeab9e8999">EditStreamCallback</a> function or a code indicating that the control encountered an error. 


### -field pfnCallback

Type: <b>EDITSTREAMCALLBACK</b>

Pointer to an <a href="https://msdn.microsoft.com/9445b141-bd0f-4bf6-8986-fbfeab9e8999">EditStreamCallback</a> function, which is an application-defined function that the control calls to transfer data. The control calls the callback function repeatedly, transferring a portion of the data with each call. 


## -see-also




<a href="https://msdn.microsoft.com/b8d3a108-b415-4f5e-99e7-0e0e7a82a778">EM_STREAMIN</a>



<a href="https://msdn.microsoft.com/3f14aaac-4b17-47af-8f2b-503390631a88">EM_STREAMOUT</a>



<a href="https://msdn.microsoft.com/9445b141-bd0f-4bf6-8986-fbfeab9e8999">EditStreamCallback</a>



<b>Reference</b>
 

 

