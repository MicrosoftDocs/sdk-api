---
UID: NF:imapi2fs.IIsoImageManager.SetStream
title: IIsoImageManager::SetStream
author: windows-sdk-content
description: Sets the Stream property with the IStream object associated with the .iso image.
old-location: imapi\iisoimagemanager_setstream.htm
tech.root: imapi
ms.assetid: 3ee540aa-8ccc-40cb-afc8-b1790cabee6e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IIsoImageManager interface [IMAPI],SetStream method, IIsoImageManager.SetStream, IIsoImageManager::SetStream, SetStream, SetStream method [IMAPI], SetStream method [IMAPI],IIsoImageManager interface, imapi.iisoimagemanager_setstream, imapi2fs/IIsoImageManager::SetStream
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
 - IIsoImageManager.SetStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2fs.h
: 
- IIsoImageManager.SetStream
: 
---

# IIsoImageManager::SetStream


## -description


Sets the <b>Stream</b> property with the <b>IStream</b> object associated with the .iso image.


## -parameters




### -param data [in, optional]

The <b>IStream</b> object associated with the .iso image.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/47b059a9-a18a-4f32-9a02-6566175ca86b">IIsoImageManager</a>



<a href="https://msdn.microsoft.com/0655edb2-5dce-4428-b883-984ef53712cd">IIsoImageManager::get_Stream</a>
 

 

