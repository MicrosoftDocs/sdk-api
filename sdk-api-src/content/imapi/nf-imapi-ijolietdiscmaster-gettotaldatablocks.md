---
UID: NF:imapi.IJolietDiscMaster.GetTotalDataBlocks
title: IJolietDiscMaster::GetTotalDataBlocks
author: windows-sdk-content
description: Retrieves the total number of blocks available for staging a Joliet data disc.
old-location: imapi\ijolietdiscmaster_gettotaldatablocks.htm
old-project: imapi
ms.assetid: fa5df4de-eecc-406b-a38d-939e7b631fc8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetTotalDataBlocks, GetTotalDataBlocks method [IMAPI], GetTotalDataBlocks method [IMAPI],IJolietDiscMaster interface, IJolietDiscMaster interface [IMAPI],GetTotalDataBlocks method, IJolietDiscMaster.GetTotalDataBlocks, IJolietDiscMaster::GetTotalDataBlocks, _win32_ijolietdiscmaster_gettotaldatablocks, base.ijolietdiscmaster_gettotaldatablocks, imapi.ijolietdiscmaster_gettotaldatablocks, imapi/IJolietDiscMaster::GetTotalDataBlocks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IJolietDiscMaster.GetTotalDataBlocks
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IJolietDiscMaster::GetTotalDataBlocks


## -description


Retrieves the total number of blocks available for staging a Joliet data disc. The data returned from this method is valid only after a 
<a href="https://msdn.microsoft.com/5f2e9135-d251-4702-b5d1-51d9b445a4f5">SetActiveDiscRecorder</a> call, especially in a multi-session burn.


## -parameters




### -param pnBlocks [out]

Total number of data blocks available on a disc.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/e2269b68-1860-4afd-90f2-d61297f3fa9b">IJolietDiscMaster</a>
 

 

