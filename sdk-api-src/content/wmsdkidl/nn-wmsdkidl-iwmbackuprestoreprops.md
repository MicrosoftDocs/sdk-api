---
UID: NN:wmsdkidl.IWMBackupRestoreProps
title: IWMBackupRestoreProps (wmsdkidl.h)
description: The IWMBackupRestoreProps interface sets and retrieves properties required by the IWMLicenseBackup and IWMLicenseRestore interfaces.
helpviewer_keywords: ["IWMBackupRestoreProps","IWMBackupRestoreProps interface [windows Media Format]","IWMBackupRestoreProps interface [windows Media Format]","described","IWMBackupRestorePropsInterface","wmformat.iwmbackuprestoreprops","wmsdkidl/IWMBackupRestoreProps"]
old-location: wmformat\iwmbackuprestoreprops.htm
tech.root: wmformat
ms.assetid: 3a5af1f3-e652-4729-931b-d0702af408f3
ms.date: 12/05/2018
ms.keywords: IWMBackupRestoreProps, IWMBackupRestoreProps interface [windows Media Format], IWMBackupRestoreProps interface [windows Media Format],described, IWMBackupRestorePropsInterface, wmformat.iwmbackuprestoreprops, wmsdkidl/IWMBackupRestoreProps
f1_keywords:
- wmsdkidl/IWMBackupRestoreProps
dev_langs:
- c++
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
- IWMBackupRestoreProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMBackupRestoreProps interface


## -description


<p class="CCE_Message">[<b>IWMBackupRestoreProps</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMBackupRestoreProps</b> interface sets and retrieves properties required by the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup">IWMLicenseBackup</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore">IWMLicenseRestore</a> interfaces.



This interface can be obtained from the backup restorer object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMBackupRestoreProps</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMBackupRestoreProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMBackupRestoreProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-getpropbyindex">GetPropByIndex</a>
</td>
<td align="left" width="63%">
Retrieves the name and value of a property by index. This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-getpropbyname">GetPropByName</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property by name. This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-getpropcount">GetPropCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties. This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-removeallprops">RemoveAllProps</a>
</td>
<td align="left" width="63%">
Removes all properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-removeprop">RemoveProp</a>
</td>
<td align="left" width="63%">
Removes one property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop">SetProp</a>
</td>
<td align="left" width="63%">
Adds a property, and sets its name and value.

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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup">IWMLicenseBackup</a>
</td>
<td>IID_IWMLicenseBackup</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore">IWMLicenseRestore</a>
</td>
<td>IID_IWMLicenseRestore</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/backup-restorer-object">Backup Restorer Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup">IWMLicenseBackup Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore">IWMLicenseRestore Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

