---
UID: NN:gpmgmt.IGPMConstants2
title: IGPMConstants2
author: windows-driver-content
description: The IGPMConstants2 interface supports methods that retrieve the value of multiple Group Policy Management Console (GPMC) constants.
old-location: gpmc\igpmconstants2.htm
old-project: GPMC
ms.assetid: daef093b-679b-411d-ba04-5d48b4695cf7
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IGPMConstants2, IGPMConstants2 interface [GPMC], IGPMConstants2 interface [GPMC], described, gpmc.igpmconstants2, gpmgmt/IGPMConstants2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMConstants2
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMConstants2 interface


## -description


The 
<b>IGPMConstants2</b> interface supports methods that retrieve the value of multiple Group Policy Management Console (GPMC) constants. The constants that are supported by <b>IGPMConstants2</b> provide Starter Group Policy object (GPO) and comment support. To create a <b>GPMConstants2</b> object, call the 
<a href="https://msdn.microsoft.com/ba271dbb-320f-409c-aff4-b7dde57f9062">IGPM::GetConstants</a> method.

The <b>GPMConstants</b> object that implements the 
<a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">IGPMConstants2</a> interface does not introduce new constants. All the constant values and the enumeration types that are  returned by the <b>GPMConstants</b> object can be found in either the GPMC header file (Gpmgmt.idl or Gpmgmt.h) or in the GPMC type library that is embedded in the Gpmgmt.dll dynamic-link library. Use the <b>GPMConstants</b> object only if you do not have access to the header or to the type library.


## -remarks



For more information about policy-related permissions, see 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a> (<b>GPM.CreatePermission</b>).




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">IGPMConstants</a>
 

 

