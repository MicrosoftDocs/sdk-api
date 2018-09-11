---
UID: NF:winsync.ISyncChangeBatchAdvanced.ConvertFullEnumerationChangeBatchToRegularChangeBatch
title: ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch
author: windows-sdk-content
description: Converts an ISyncFullEnumerationChangeBatch object to an ISyncChangeBatch object.
old-location: winsync\isyncchangebatchadvanced_convertfullenumerationchangebatchtoregularchangebatch.htm
tech.root: winsync
ms.assetid: 073369ab-232e-410f-b6f1-c43bf15cc652
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ConvertFullEnumerationChangeBatchToRegularChangeBatch, ConvertFullEnumerationChangeBatchToRegularChangeBatch method [Windows Sync], ConvertFullEnumerationChangeBatchToRegularChangeBatch method [Windows Sync],ISyncChangeBatchAdvanced interface, ISyncChangeBatchAdvanced interface [Windows Sync],ConvertFullEnumerationChangeBatchToRegularChangeBatch method, ISyncChangeBatchAdvanced.ConvertFullEnumerationChangeBatchToRegularChangeBatch, ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch, winsync.isyncchangebatchadvanced_convertfullenumerationchangebatchtoregularchangebatch, winsync/ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncChangeBatchAdvanced.ConvertFullEnumerationChangeBatchToRegularChangeBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch


## -description


Converts an <a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch</a> object to an <a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch</a> object.


## -parameters




### -param ppChangeBatch [out]

Returns this change batch object, which is represented as an <a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch</a> object.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
This change batch object is not an <a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch</a> object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/b78bc885-ed4e-4c83-ad1b-043c5b226337">ISyncChangeBatchAdvanced Interface</a>



<a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch Interface</a>
 

 

