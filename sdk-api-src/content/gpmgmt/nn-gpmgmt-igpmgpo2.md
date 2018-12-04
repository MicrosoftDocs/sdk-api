---
UID: NN:gpmgmt.IGPMGPO2
title: IGPMGPO2
author: windows-sdk-content
description: The IGPMGPO2 interface supports methods that enable you to manage Group Policy objects (GPOs) and Starter Group Policy objects in the directory service.
old-location: gpmc\igpmgpo2.htm
tech.root: gpmc
ms.assetid: c5c21ca6-2722-4821-8760-03b6cf2befa7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IGPMGPO2, IGPMGPO2 interface [GPMC], IGPMGPO2 interface [GPMC],described, gpmc.igpmgpo2, gpmgmt/IGPMGPO2
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
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMGPO2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPO2 interface


## -description


The 
<b>IGPMGPO2</b> interface supports methods that enable you to manage Group Policy objects (GPOs) and Starter Group Policy objects in the directory service.

Note that you cannot use this interface to manage local GPOs (LGPOs).

You can instantiate a <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO2</a> object by creating a new one with a call to 
<a href="https://msdn.microsoft.com/00e83637-820b-488e-abf4-4210ac3b98b6">IGPMDomain::CreateGPO</a>, or  <b>IGPMDomain2::CreateStarterGPO</b> retrieving an existing one with a call to 
<a href="https://msdn.microsoft.com/ac413241-3649-4f22-9a67-94e4da8672e7">IGPMDomain::GetGPO</a>, calling <b>IGPMDomain2::GetStarterGPO</b> or by searching for one with a call to 
<a href="https://msdn.microsoft.com/19a8efae-0b85-49ba-bf7e-08ed700874c3">IGPMDomain::SearchGPOs</a>. You can also create a GPO from an existing Starter GPO with a call to <b>IGPMDomain2::CreateGPOFromStarterGPO</b>. After creating the object, you can query the GPO and set properties related to the GPO.


## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<b>IGPMDomain2</b>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">IGPMGPOCollection</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>
 

 

