---
UID: NN:vsmgmt.IVssSnapshotMgmt2
title: IVssSnapshotMgmt2
author: windows-sdk-content
description: Provides a method to retrieve the minimum size of the shadow copy storage area.
old-location: base\ivsssnapshotmgmt2.htm
old-project: VSS
ms.assetid: 92c8c960-d548-4a44-8b10-b6180c974473
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssSnapshotMgmt2, IVssSnapshotMgmt2 interface [Files], IVssSnapshotMgmt2 interface [Files],described, base.ivsssnapshotmgmt2, vsmgmt/IVssSnapshotMgmt2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vsmgmt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: VSS_PROTECTION_LEVEL, *PVSS_PROTECTION_LEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsMgmt.h
api_name:
 - IVssSnapshotMgmt2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssSnapshotMgmt2 interface


## -description


The <b>IVssSnapshotMgmt2</b> interface 
    provides a method to retrieve the minimum size of the shadow copy storage area.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssSnapshotMgmt2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssSnapshotMgmt2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssSnapshotMgmt2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1ee4499-07cb-4373-a3c9-892129a257db">GetMinDiffAreaSize</a>
</td>
<td align="left" width="63%">
Returns the current minimum size of the shadow copy storage area.</p> (Inherited from <b>IVssSnapshotMgmt2</b>)</td>
</tr>
</table> 


## -remarks



To obtain an instance of the <b>IVssSnapshotMgmt2</b> 
   interface, call the <a href="_com_iunknown_queryinterface">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/5e5694a1-7c17-4d8a-b094-09dcf28a636f">IVssSnapshotMgmt</a> interface, passing 
   <b>IID_IVssSnapshotMgmt2</b> as the <i>riid</i> parameter.




## -see-also




<a href="_com_iunknown">IUnknown</a>



<a href="https://msdn.microsoft.com/3a0c60df-666c-4e33-a54c-7fa5ddbfde13">Volume Shadow Copy API Interfaces</a>
 

 

