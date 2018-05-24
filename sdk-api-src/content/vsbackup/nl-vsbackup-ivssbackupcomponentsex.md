---
UID: NL:vsbackup.IVssBackupComponentsEx
title: IVssBackupComponentsEx
author: windows-driver-content
description: Provides methods for requesters to run backup and restore operations using multiple writer instances.
old-location: base\ivssbackupcomponentsex.htm
old-project: VSS
ms.assetid: d3a265ab-39cc-4861-9191-9ecf094d8826
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IVssBackupComponentsEx, IVssBackupComponentsEx interface [VSS], IVssBackupComponentsEx interface [VSS],described, base.ivssbackupcomponentsex, vsbackup/IVssBackupComponentsEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssBackupComponentsEx
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: VssApi.dll
req.irql: 
req.product: Windows UI
---

# IVssBackupComponentsEx class


## -description


The <b>IVssBackupComponentsEx</b> interface provides methods for requesters to run backup and restore operations using multiple writer instances.

To obtain an instance of the <b>IVssBackupComponentsEx</b> 
   interface, call the <a href="_com_iunknown_queryinterface">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> interface, passing 
   <b>IID_IVssBackupComponentsEx</b> as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssBackupComponentsEx</b> interface inherits from <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>. <b>IVssBackupComponentsEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssBackupComponentsEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19a31627-54e0-4b0d-87cf-ac18b3049310">GetWriterMetadataEx</a>
</td>
<td align="left" width="63%">
Returns writer metadata for a specific writer instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/469e6d61-85c6-4385-92be-df6addefe37f">SetSelectedForRestoreEx</a>
</td>
<td align="left" width="63%">
Indicates whether the specified component has been selected for restoration to a specified writer instance.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>
 

 

