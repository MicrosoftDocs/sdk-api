---
UID: NN:wmsdkidl.IWMLicenseRestore
title: IWMLicenseRestore
author: windows-sdk-content
description: The IWMLicenseRestore interface manages the restoring of licenses.This interface is obtained from another interface on the backup restorer object.
old-location: wmformat\iwmlicenserestore.htm
old-project: wmformat
ms.assetid: 29444445-7104-4900-a00d-dabd2766d1d7
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMLicenseRestore, IWMLicenseRestore interface [windows Media Format], IWMLicenseRestore interface [windows Media Format],described, IWMLicenseRestoreInterface, wmformat.iwmlicenserestore, wmsdkidl/IWMLicenseRestore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMLicenseRestore
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMLicenseRestore interface


## -description


<p class="CCE_Message">[<b>IWMLicenseRestore</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMLicenseRestore</b> interface manages the restoring of licenses.

This interface is obtained from another interface on the backup restorer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMLicenseRestore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMLicenseRestore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMLicenseRestore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8a39804-5ee6-43ab-8e89-d1008217622d">CancelLicenseRestore</a>
</td>
<td align="left" width="63%">
Cancels a current restore operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d645b3a-e856-4745-b80a-89a3bc2b38bd">RestoreLicenses</a>
</td>
<td align="left" width="63%">
Restores licenses that were previously backed up.

</td>
</tr>
</table> 

The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3a5af1f3-e652-4729-931b-d0702af408f3">IWMBackupRestoreProps</a>
</td>
<td>IID_IWMBackupRestoreProps</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4ef43b7e-706b-48f6-80ba-7d0a59c3929a">IWMLicenseBackup</a>
</td>
<td>IID_IWMLicenseBackup</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/59be02fe-f207-4161-8765-9a88a8050248">Backing Up and Restoring Licenses</a>



<a href="https://msdn.microsoft.com/83ce28c0-fd17-46ff-94c0-d28124a0e56a">Backup Restorer Object</a>



<a href="https://msdn.microsoft.com/3a5af1f3-e652-4729-931b-d0702af408f3">IWMBackupRestoreProps Interface</a>



<a href="https://msdn.microsoft.com/4ef43b7e-706b-48f6-80ba-7d0a59c3929a">IWMLicenseBackup Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

