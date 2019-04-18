---
UID: NF:imapi2fs.IIsoImageManager.SetPath
title: IIsoImageManager::SetPath (imapi2fs.h)
author: windows-sdk-content
description: Sets the Path property value with a logical path to an .iso image.
old-location: imapi\iisoimagemanager_setpath.htm
tech.root: imapi
ms.assetid: 3e5ef908-795d-4617-8123-605855b9ddc8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsoImageManager interface [IMAPI],SetPath method, IIsoImageManager.SetPath, IIsoImageManager::SetPath, SetPath, SetPath method [IMAPI], SetPath method [IMAPI],IIsoImageManager interface, imapi.iisoimagemanager_setpath, imapi2fs/IIsoImageManager::SetPath
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
req.idl: Imapi2.idl
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
 - imapi2fs.h
api_name:
 - IIsoImageManager.SetPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsoImageManager::SetPath


## -description


Sets the <b>Path</b> property value  with a logical path to an .iso image.


## -parameters




### -param Val [in]

The logical path to the .iso image. For example, "c:\\path\\file.iso".


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_PATH</b></dt>
</dl>
</td>
<td width="60%">
Path '%1!s!' is badly formed or contains invalid characters.

Value: 0xC0AAB110

</td>
</tr>
</table>
 




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/47b059a9-a18a-4f32-9a02-6566175ca86b">IIsoImageManager</a>



<a href="https://msdn.microsoft.com/56166789-8eeb-4468-a85e-b35e665170d6">IIsoImageManager::get_Path</a>
 

 

