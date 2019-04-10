---
UID: NN:wmsdkidl.IWMLicenseRestore
title: IWMLicenseRestore (wmsdkidl.h)
author: windows-sdk-content
description: The IWMLicenseRestore interface manages the restoring of licenses.This interface is obtained from another interface on the backup restorer object.
old-location: wmformat\iwmlicenserestore.htm
tech.root: wmformat
ms.assetid: 29444445-7104-4900-a00d-dabd2766d1d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMLicenseRestore, IWMLicenseRestore interface [windows Media Format], IWMLicenseRestore interface [windows Media Format],described, IWMLicenseRestoreInterface, wmformat.iwmlicenserestore, wmsdkidl/IWMLicenseRestore
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMLicenseRestore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dd757223(v=VS.85).aspx">CancelLicenseRestore</a>
</td>
<td align="left" width="63%">
Cancels a current restore operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757224(v=VS.85).aspx">RestoreLicenses</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd743291(v=VS.85).aspx">IWMBackupRestoreProps</a>
</td>
<td>IID_IWMBackupRestoreProps</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757218(v=VS.85).aspx">IWMLicenseBackup</a>
</td>
<td>IID_IWMLicenseBackup</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/59be02fe-f207-4161-8765-9a88a8050248">Backing Up and Restoring Licenses</a>



<a href="https://msdn.microsoft.com/83ce28c0-fd17-46ff-94c0-d28124a0e56a">Backup Restorer Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743291(v=VS.85).aspx">IWMBackupRestoreProps Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757218(v=VS.85).aspx">IWMLicenseBackup Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

