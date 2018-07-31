---
UID: NF:winddi.DrvIcmDeleteColorTransform
title: DrvIcmDeleteColorTransform function
author: windows-sdk-content
description: The DrvIcmDeleteColorTransform function deletes the specified color transform.
old-location: display\drvicmdeletecolortransform.htm
old-project: display
ms.assetid: aa1226d3-7b2a-4911-b785-eea9f72016f5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DrvIcmDeleteColorTransform, DrvIcmDeleteColorTransform function [Display Devices], ddifncs_883d2f55-a3e0-4682-a099-8fef07b6e3a7.xml, display.drvicmdeletecolortransform, winddi/DrvIcmDeleteColorTransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvIcmDeleteColorTransform
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvIcmDeleteColorTransform function


## -description


The <b>DrvIcmDeleteColorTransform</b> function deletes the specified color transform.


## -parameters




### -param dhpdev [in]

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>.


### -param hcmXform [in]

Handle to the color transform to be deleted. This color transform was created by the driver in a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>.


## -returns



<b>DrvIcmDeleteColorTransform</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



Drivers that report ICM support should implement this function. A driver indicates support for ICM by setting the GCAPS_ICM flag in the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>
 

 

