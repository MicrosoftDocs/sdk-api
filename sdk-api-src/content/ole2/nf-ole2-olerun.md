---
UID: NF:ole2.OleRun
title: OleRun function
author: windows-sdk-content
description: Puts an OLE compound document object into the running state.
old-location: com\olerun.htm
old-project: com
ms.assetid: 9035f996-b163-4855-aa9d-184b77072ead
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: OleRun, OleRun function [COM], _ole_OleRun, com.olerun, ole2/OleRun
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-OLE32-IE-l1-1-0.dll
 - ole32_wp.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleRun
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleRun function


## -description


Puts an OLE compound document object into the running state.


## -parameters




### -param pUnknown [in]

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the object, with which it will query for a pointer to the <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a> interface, and then call its <a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a> method.


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
<dt><b>OLE_E_CLASSDIFF</b></dt>
</dl>
</td>
<td width="60%">
The source of an OLE link has been converted to a different class.

</td>
</tr>
</table>
 




## -remarks



The <b>OleRun</b> function puts an object in the running state. The implementation of <b>OleRun</b> was changed in OLE 2.01 to coincide with the publication of the <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a> interface. You can use <b>OleRun</b> and <a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">IRunnableObject::Run</a> interchangeably. <b>OleRun</b> queries the object for a pointer to <b>IRunnableObject</b>. If successful, the function returns the results of calling the <b>IRunnableObject::Run</b> method.

For more information on using this function, see <a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">IRunnableObject::Run</a>.




## -see-also




<a href="https://msdn.microsoft.com/1fadd27d-cb2c-47fc-891a-16f82bdac0f6">IOleLink::BindToSource</a>



<a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">IRunnableObject::Run</a>
 

 

