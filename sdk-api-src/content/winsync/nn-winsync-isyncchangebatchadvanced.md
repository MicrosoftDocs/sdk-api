---
UID: NN:winsync.ISyncChangeBatchAdvanced
title: ISyncChangeBatchAdvanced (winsync.h)
author: windows-sdk-content
description: Represents additional information about a set of changes.
old-location: winsync\isyncchangebatchadvanced.htm
tech.root: winsync
ms.assetid: b78bc885-ed4e-4c83-ad1b-043c5b226337
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchAdvanced, ISyncChangeBatchAdvanced interface [Windows Sync], ISyncChangeBatchAdvanced interface [Windows Sync],described, winsync.isyncchangebatchadvanced, winsync/ISyncChangeBatchAdvanced
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
 - ISyncChangeBatchAdvanced
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeBatchAdvanced interface


## -description


Represents additional information about a set of changes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeBatchAdvanced</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncChangeBatchAdvanced</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeBatchAdvanced</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/073369ab-232e-410f-b6f1-c43bf15cc652">ConvertFullEnumerationChangeBatchToRegularChangeBatch</a>
</td>
<td align="left" width="63%">
Converts an <a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch</a> object to an <a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch</a> object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/911ac2dd-a8df-4f71-81da-032219664453">GetBatchLevelKnowledgeShouldBeApplied</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the learned knowledge for the batch must be saved after the batch is applied to the destination replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f630f806-cc5a-408e-bd84-49555ebb41c1">GetFilterInfo</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo</a> that was specified when the change batch was created.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4aa472b1-7dfb-4159-8f50-cc8e5de34dd3">GetUpperBoundItemId</a>
</td>
<td align="left" width="63%">
Gets the highest item ID that is represented in the knowledge of any group in the change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/">RemapKnowledges</a>
</td>
<td align="left" width="63%">
Remaps all knowledge objects that are contained in the change batch so that they are relative to the replica key map of the specified knowledge.


</td>
</tr>
</table> 


## -remarks



An <b>ISyncChangeBatchAdvanced</b> object can be obtained by passing <b>IID_ISyncChangeBatchAdvanced</b> to the <b>QueryInterface</b> method of a change batch object, such as an <a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch</a> or <a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch</a> object.




## -see-also




<a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>



<a href="https://msdn.microsoft.com/45f10ed0-b3ce-41f5-b2d9-9166bff2abec">ISyncChangeBatchBase2 Interface</a>



<a href="https://msdn.microsoft.com/29d767cf-3261-4550-8b28-5d3950b8ded1">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo Interface</a>



<a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

