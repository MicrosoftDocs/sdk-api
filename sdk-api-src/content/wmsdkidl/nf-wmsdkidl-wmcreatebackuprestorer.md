---
UID: NF:wmsdkidl.WMCreateBackupRestorer
title: WMCreateBackupRestorer function
author: windows-driver-content
description: The WMCreateBackupRestorer function creates a backup restorer object.
old-location: wmformat\wmcreatebackuprestorer.htm
old-project: wmformat
ms.assetid: 529a5066-df03-4747-bca5-10e3f223d4d2
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WMCreateBackupRestorer, WMCreateBackupRestorer function [windows Media Format], wmformat.wmcreatebackuprestorer, wmsdkidl/WMCreateBackupRestorer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
-	DllExport
api_location:
-	Wmvcore.dll
api_name:
-	WMCreateBackupRestorer
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMCreateBackupRestorer function


## -description



The <b>WMCreateBackupRestorer</b> function creates a backup restorer object.




## -parameters




### -param pCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3">IWMStatusCallback</a> interface containing the <b>OnStatus</b> callback method to be used by the new backup restorer object.


### -param ppBackup [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/4ef43b7e-706b-48f6-80ba-7d0a59c3929a">IWMLicenseBackup</a> interface of the newly created backup restorer object.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -remarks



Use <b>IWMLicenseBackup::QueryInterface</b> to obtain a pointer to the <a href="https://msdn.microsoft.com/3a5af1f3-e652-4729-931b-d0702af408f3">IWMBackupRestoreProps</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/83ce28c0-fd17-46ff-94c0-d28124a0e56a">Backup Restorer Object</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

