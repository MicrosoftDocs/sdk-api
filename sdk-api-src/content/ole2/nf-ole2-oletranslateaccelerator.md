---
UID: NF:ole2.OleTranslateAccelerator
title: OleTranslateAccelerator function
author: windows-sdk-content
description: Called by the object application, allows an object's container to translate accelerators according to the container's accelerator table.
old-location: com\oletranslateaccelerator.htm
tech.root: com
ms.assetid: c590efef-7f03-4ae6-a35f-eff2fc4da3d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OleTranslateAccelerator, OleTranslateAccelerator function [COM], _ole_OleTranslateAccelerator, com.oletranslateaccelerator, ole2/OleTranslateAccelerator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-Com-OLE32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleTranslateAccelerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleTranslateAccelerator function


## -description


Called by the object application, allows an object's container to translate accelerators according to the container's accelerator table.




## -parameters




### -param lpFrame [in]

Pointer to the <a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a> interface to which the keystroke might be sent.


### -param lpFrameInfo [in]

Pointer to an <a href="https://msdn.microsoft.com/e09445d2-61e5-4691-b51e-746e0cc91c00">OLEINPLACEFRAMEINFO</a> structure containing the accelerator table obtained from the container.


### -param lpmsg [in]

Pointer to an <a href="_win32_MSG_str_cpp">MSG</a> structure containing the keystroke.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The object should continue processing this message.


</td>
</tr>
</table>
 




## -remarks



Object servers call <b>OleTranslateAccelerator</b> to allow the object's container to translate accelerator keystrokes according to the container's accelerator table, pointed to by <i>lpFrameInfo</i>. While a contained object is the active object, the object's server always has first chance at translating any messages received. If this is not desired, the server calls <b>OleTranslateAccelerator</b> to give the object's container a chance. If the keyboard input matches an accelerator found in the container-provided accelerator table, <b>OleTranslateAccelerator</b> passes the message and its command identifier on to the container through the <a href="https://msdn.microsoft.com/f755b919-b810-4b66-b3c2-bf38bd525d60">IOleInPlaceFrame::TranslateAccelerator</a> method. This method returns S_OK if the keystroke is consumed; otherwise it returns S_FALSE.



Accelerator tables for containers should be defined so they will work properly with object applications that do their own accelerator keystroke translations. These tables should take the form:

<pre class="syntax" xml:space="preserve"><code>"char", wID, VIRTKEY, CONTROL</code></pre>
This is the most common way to describe keyboard accelerators. Failure to do so can result in keystrokes being lost or sent to the wrong object during an in-place session.

Objects can call the <a href="https://msdn.microsoft.com/2d09f81a-b422-4379-89c8-d50992ebb24c">IsAccelerator</a> function to see whether the accelerator keystroke belongs to the object or the container. 





## -see-also




<a href="https://msdn.microsoft.com/f755b919-b810-4b66-b3c2-bf38bd525d60">IOleInPlaceFrame::TranslateAccelerator</a>



<a href="https://msdn.microsoft.com/2d09f81a-b422-4379-89c8-d50992ebb24c">IsAccelerator</a>
 

 

