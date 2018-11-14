---
UID: NN:winsync.ISyncChangeBatchBase2
title: ISyncChangeBatchBase2
author: windows-sdk-content
description: Represents additional capabilities of an ISyncChangeBatchBase object.
old-location: winsync\isyncchangebatchbase2.htm
tech.root: winsync
ms.assetid: 45f10ed0-b3ce-41f5-b2d9-9166bff2abec
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISyncChangeBatchBase2, ISyncChangeBatchBase2 interface [Windows Sync], ISyncChangeBatchBase2 interface [Windows Sync],described, winsync.isyncchangebatchbase2, winsync/ISyncChangeBatchBase2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ISyncChangeBatchBase2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncChangeBatchBase2 interface


## -description


Represents additional capabilities of an <a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeBatchBase2</b> interface inherits from <a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase</a>. <b>ISyncChangeBatchBase2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeBatchBase2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e686e6f-08b1-4a58-ac0f-30c48f70dd60">SerializeWithOptions</a>
</td>
<td align="left" width="63%">
Serializes the change batch object data to a byte array based on the specified version and serialization options.

</td>
</tr>
</table> 


## -remarks



An <b>ISyncChangeBatchBase2</b> object can be obtained by passing <b>IID_ISyncChangeBatchBase2</b> to the <b>QueryInterface</b> method of an <a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase</a> object.





## -see-also




<a href="https://msdn.microsoft.com/c3f27c6d-4fc1-420c-afc1-0bd2bdbd6ab2">IEnumSyncChanges Interface</a>



<a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/b78bc885-ed4e-4c83-ad1b-043c5b226337">ISyncChangeBatchAdvanced Interface</a>



<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>



<a href="https://msdn.microsoft.com/29d767cf-3261-4550-8b28-5d3950b8ded1">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/840a1f5e-56f7-4774-a154-0dab66c3d407">SyncSerializationVersion Enumeration</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

