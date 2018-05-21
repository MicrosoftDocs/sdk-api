---
UID: NF:imapi2fs.IFileSystemImage.SetMaxMediaBlocksFromDevice
title: IFileSystemImage::SetMaxMediaBlocksFromDevice
author: windows-driver-content
description: Set maximum number of blocks available based on the capabilities of the recorder.
old-location: imapi\ifilesystemimage_setmaxmediablocksfromdevice.htm
old-project: imapi
ms.assetid: 201e7390-68f3-48a4-9036-b07219fa3d80
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFileSystemImage interface [IMAPI],SetMaxMediaBlocksFromDevice method, IFileSystemImage.SetMaxMediaBlocksFromDevice, IFileSystemImage::SetMaxMediaBlocksFromDevice, SetMaxMediaBlocksFromDevice, SetMaxMediaBlocksFromDevice method [IMAPI], SetMaxMediaBlocksFromDevice method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_setmaxmediablocksfromdevice, imapi2fs/IFileSystemImage::SetMaxMediaBlocksFromDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFileSystemImage.SetMaxMediaBlocksFromDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::SetMaxMediaBlocksFromDevice


## -description


Set maximum number of blocks available based on the capabilities of the recorder.


## -parameters




### -param discRecorder






#### - discRecorder2 [in]

An <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> interface that identifies the recording device from which you want to set the maximum number of blocks available. 


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_FSI_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Internal error occurred: <i>%1!ls!</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>
 

 

