---
UID: NF:ole2.OleIsCurrentClipboard
title: OleIsCurrentClipboard function
author: windows-sdk-content
description: Determines whether the data object pointer previously placed on the clipboard by the OleSetClipboard function is still on the clipboard.
old-location: com\oleiscurrentclipboard.htm
tech.root: com
ms.assetid: 12844504-ef47-4a4d-b31b-f765e0f2ace6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OleIsCurrentClipboard, OleIsCurrentClipboard function [COM], _ole_OleIsCurrentClipboard, com.oleiscurrentclipboard, ole2/OleIsCurrentClipboard
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
 - API-MS-Win-RTCore-OLE32-clipboard-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-ole32-clipboard-ie-l1-1-0.dll
 - API-MS-Win-RTCore-Ole32-Clipboard-L1-1-1.dll
api_name:
 - OleIsCurrentClipboard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleIsCurrentClipboard function


## -description


Determines whether the data object pointer previously placed on the clipboard by the <a href="https://msdn.microsoft.com/741def10-d2b5-4395-8049-1eba2e29b0e8">OleSetClipboard</a> function is still on the clipboard.




## -parameters




### -param pDataObj [in]

Pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object containing clipboard data of interest, which the caller previously placed on the clipboard.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer is not on the clipboard.


</td>
</tr>
</table>
 




## -remarks



<b>OleIsCurrentClipboard</b> only works for the data object used in the <a href="https://msdn.microsoft.com/741def10-d2b5-4395-8049-1eba2e29b0e8">OleSetClipboard</a> function. It cannot be called by the consumer of the data object to determine if the object that was on the clipboard at the previous <a href="https://msdn.microsoft.com/c5e7badb-339b-48d5-8c9a-3950e2ffe6bf">OleGetClipboard</a> call is still on the clipboard.




## -see-also




<a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a>



<a href="https://msdn.microsoft.com/741def10-d2b5-4395-8049-1eba2e29b0e8">OleSetClipboard</a>
 

 

