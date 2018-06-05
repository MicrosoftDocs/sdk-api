---
UID: NL:vsbackup.IVssBackupComponentsEx4
title: IVssBackupComponentsEx4
author: windows-sdk-content
description: Defines additional methods to support the processing of UNC file share paths in a requester.
old-location: base\ivssbackupcomponentsex4.htm
old-project: VSS
ms.assetid: 3D72F6FC-4EAA-49F9-9652-AC314FFAB504
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssBackupComponentsEx4, IVssBackupComponentsEx4 interface, IVssBackupComponentsEx4 interface,described, base.ivssbackupcomponentsex4, vsbackup/IVssBackupComponentsEx4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VsBackup.h
api_name:
-	IVssBackupComponentsEx4
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: VssApi.dll
req.irql: 
req.product: Windows UI
---

# IVssBackupComponentsEx4 class


## -description


Defines additional methods to support the processing of UNC file share paths in a requester.

To obtain an instance of the <b>IVssBackupComponentsEx4</b> 
   interface, call the <a href="_com_iunknown_queryinterface">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> interface, and pass 
   the <b>IID_IVssBackupComponentsEx4</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssBackupComponentsEx4</b> interface inherits from <a href="https://msdn.microsoft.com/56c8e7c2-2d94-4674-bd20-bf036991474f">IVssBackupComponentsEx3</a>, <a href="https://msdn.microsoft.com/69d4d500-0e21-48bd-b90b-d06c88fde136">IVssBackupComponentsEx2</a>, <a href="https://msdn.microsoft.com/d3a265ab-39cc-4861-9191-9ecf094d8826">IVssBackupComponentsEx</a>, and <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>. <b>IVssBackupComponentsEx4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssBackupComponentsEx4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94F942A9-909D-4A9F-9DEA-CFFCFD00C1BF">GetRootAndLogicalPrefixPaths</a>
</td>
<td align="left" width="63%">
Normalizes a local volume path or UNC share path so that it can be passed to the <a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/d3a265ab-39cc-4861-9191-9ecf094d8826">IVssBackupComponentsEx</a>



<a href="https://msdn.microsoft.com/69d4d500-0e21-48bd-b90b-d06c88fde136">IVssBackupComponentsEx2</a>



<a href="https://msdn.microsoft.com/56c8e7c2-2d94-4674-bd20-bf036991474f">IVssBackupComponentsEx3</a>
 

 

