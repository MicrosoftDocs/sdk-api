---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvUnInitializeWia
title: IWiaMiniDrv::drvUnInitializeWia method
author: windows-driver-content
description: The IWiaMiniDrv::drvUnInitializeWia method releases resources held by the minidriver.
old-location: image\iwiaminidrv_drvuninitializewia.htm
old-project: image
ms.assetid: 974de3b5-c129-42ee-a522-071c26726cf1
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvUnInitializeWia method, IWiaMiniDrv::drvUnInitializeWia, MiniDrv_2a06b98b-7b47-46d8-b158-8e6ff6bac6b9.xml, drvUnInitializeWia method [Imaging Devices], drvUnInitializeWia method [Imaging Devices], IWiaMiniDrv interface, drvUnInitializeWia,IWiaMiniDrv.drvUnInitializeWia, image.iwiaminidrv_drvuninitializewia, wiamindr_lh/IWiaMiniDrv::drvUnInitializeWia
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SCANWINDOW, *PSCANWINDOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wiamindr_lh.h
api_name:
-	IWiaMiniDrv.drvUnInitializeWia
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvUnInitializeWia method


## -description


The <b>IWiaMiniDrv::drvUnInitializeWia</b> method releases resources held by the minidriver.


## -parameters




### -param __MIDL__IWiaMiniDrv0064






#### - pWiasContext [in]

Pointer to a WIA item context.


## -returns



On success, the method should return S_OK If the method fails, it should return a standard COM error code.




## -remarks



The WIA service calls the <b>IWiaMiniDrv::drvUnInitializeWia</b> method when the resources associated with an application item tree are no longer needed. The minidriver can then unload any DLLs and free any allocated memory.




## -see-also




<a href="https://msdn.microsoft.com/15068d10-5e24-427c-9684-24ce67b75ada">IWiaMiniDrv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544986">IWiaMiniDrv::drvInitializeWia</a>
 

 

