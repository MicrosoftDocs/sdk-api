---
UID: NF:imapi.IJolietDiscMaster.GetDataBlockSize
title: IJolietDiscMaster::GetDataBlockSize method
author: windows-driver-content
description: Retrieves the size of a data block.
old-location: imapi\ijolietdiscmaster_getdatablocksize.htm
old-project: imapi
ms.assetid: 84bb0330-770d-44ab-8829-e81616f7c805
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetDataBlockSize method [IMAPI], GetDataBlockSize method [IMAPI], IJolietDiscMaster interface, GetDataBlockSize,IJolietDiscMaster.GetDataBlockSize, IJolietDiscMaster, IJolietDiscMaster interface [IMAPI], GetDataBlockSize method, IJolietDiscMaster::GetDataBlockSize, _win32_ijolietdiscmaster_getdatablocksize, base.ijolietdiscmaster_getdatablocksize, imapi.ijolietdiscmaster_getdatablocksize, imapi/IJolietDiscMaster::GetDataBlockSize
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
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Actxprxy.dll
api_name:
-	IJolietDiscMaster.GetDataBlockSize
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IJolietDiscMaster::GetDataBlockSize method


## -description


Retrieves the size of a data block.


## -parameters




### -param pnBlockBytes [out]

Total size of a single data block, in bytes.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:
					




## -remarks



This method returns 2048.




## -see-also




<a href="https://msdn.microsoft.com/e2269b68-1860-4afd-90f2-d61297f3fa9b">IJolietDiscMaster</a>
 

 

