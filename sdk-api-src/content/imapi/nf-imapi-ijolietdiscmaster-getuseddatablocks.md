---
UID: NF:imapi.IJolietDiscMaster.GetUsedDataBlocks
title: IJolietDiscMaster::GetUsedDataBlocks
author: windows-sdk-content
description: Retrieves the total number of data blocks that are in use.
old-location: imapi\ijolietdiscmaster_getuseddatablocks.htm
tech.root: imapi
ms.assetid: 01bde64a-3d91-4830-bd93-f3fe6b109264
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetUsedDataBlocks, GetUsedDataBlocks method [IMAPI], GetUsedDataBlocks method [IMAPI],IJolietDiscMaster interface, IJolietDiscMaster interface [IMAPI],GetUsedDataBlocks method, IJolietDiscMaster.GetUsedDataBlocks, IJolietDiscMaster::GetUsedDataBlocks, _win32_ijolietdiscmaster_getuseddatablocks, base.ijolietdiscmaster_getuseddatablocks, imapi.ijolietdiscmaster_getuseddatablocks, imapi/IJolietDiscMaster::GetUsedDataBlocks
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IJolietDiscMaster.GetUsedDataBlocks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IJolietDiscMaster::GetUsedDataBlocks


## -description


Retrieves the total number of data blocks that are in use. The data returned from this method is valid only after a 
<a href="https://msdn.microsoft.com/5f2e9135-d251-4702-b5d1-51d9b445a4f5">SetActiveDiscRecorder</a> call, especially in a multi-session burn.


## -parameters




### -param pnBlocks [out]

Total number of data blocks in use in the staged image.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/e2269b68-1860-4afd-90f2-d61297f3fa9b">IJolietDiscMaster</a>
 

 

