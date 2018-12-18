---
UID: NN:wmsdkidl.IWMBackupRestoreProps
title: IWMBackupRestoreProps
author: windows-sdk-content
description: The IWMBackupRestoreProps interface sets and retrieves properties required by the IWMLicenseBackup and IWMLicenseRestore interfaces.
old-location: wmformat\iwmbackuprestoreprops.htm
tech.root: wmformat
ms.assetid: 3a5af1f3-e652-4729-931b-d0702af408f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMBackupRestoreProps, IWMBackupRestoreProps interface [windows Media Format], IWMBackupRestoreProps interface [windows Media Format],described, IWMBackupRestorePropsInterface, wmformat.iwmbackuprestoreprops, wmsdkidl/IWMBackupRestoreProps
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
 - IWMBackupRestoreProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMBackupRestoreProps interface


## -description


<p class="CCE_Message">[<b>IWMBackupRestoreProps</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMBackupRestoreProps</b> interface sets and retrieves properties required by the <a href="https://msdn.microsoft.com/en-us/library/Dd757218(v=VS.85).aspx">IWMLicenseBackup</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd757221(v=VS.85).aspx">IWMLicenseRestore</a> interfaces.



This interface can be obtained from the backup restorer object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMBackupRestoreProps</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMBackupRestoreProps</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/96376e63-3c36-4bea-8cd2-362bb1ba054f">GetPropByIndex</a>
</td>
<td align="left" width="63%">
Retrieves the name and value of a property by index. This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743293(v=VS.85).aspx">GetPropByName</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property by name. This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743294(v=VS.85).aspx">GetPropCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties. This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743295(v=VS.85).aspx">RemoveAllProps</a>
</td>
<td align="left" width="63%">
Removes all properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743296(v=VS.85).aspx">RemoveProp</a>
</td>
<td align="left" width="63%">
Removes one property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743297(v=VS.85).aspx">SetProp</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd757218(v=VS.85).aspx">IWMLicenseBackup</a>
</td>
<td>IID_IWMLicenseBackup</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757221(v=VS.85).aspx">IWMLicenseRestore</a>
</td>
<td>IID_IWMLicenseRestore</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/83ce28c0-fd17-46ff-94c0-d28124a0e56a">Backup Restorer Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757218(v=VS.85).aspx">IWMLicenseBackup Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757221(v=VS.85).aspx">IWMLicenseRestore Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

