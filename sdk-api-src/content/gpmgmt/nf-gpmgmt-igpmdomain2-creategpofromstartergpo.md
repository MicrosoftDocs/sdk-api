---
UID: NF:gpmgmt.IGPMDomain2.CreateGPOFromStarterGPO
title: IGPMDomain2::CreateGPOFromStarterGPO
author: windows-sdk-content
description: Creates and retrieves a GPMGPO object from a GPMStarterGPO object.
old-location: gpmc\igpmdomain2_creategpofromstartergpo.htm
old-project: GPMC
ms.assetid: 3a74f763-a9f5-4e93-94fb-7ef2a116c82b
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: CreateGPOFromStarterGPO, CreateGPOFromStarterGPO method [GPMC], CreateGPOFromStarterGPO method [GPMC],IGPMDomain2 interface, IGPMDomain2 interface [GPMC],CreateGPOFromStarterGPO method, IGPMDomain2.CreateGPOFromStarterGPO, IGPMDomain2::CreateGPOFromStarterGPO, gpmc.igpmdomain2_creategpofromstartergpo, gpmgmt/IGPMDomain2::CreateGPOFromStarterGPO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gpmgmt.dll
api_name:
 - IGPMDomain2.CreateGPOFromStarterGPO
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMDomain2::CreateGPOFromStarterGPO


## -description


Creates and retrieves a 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object from a <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object. This method creates a new <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object. Then, this method copies the contents of the <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object into the <b>GPMGPO</b> object. Finally, this method updates the appropriate attributes of the <b>GPMGPO</b> object to reflect the configured data.


## -parameters




### -param pGPOTemplate [in]

A pointer to a <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object from which the new Group Policy object (GPO) will be created.


### -param ppnewGPO [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object that represents the new GPO.


#### - objGPMStarterGPO [in]

A reference to a <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object from which the new GPO will be created.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a>  object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a>  object.




## -see-also




<a href="https://msdn.microsoft.com/5abfea14-0cb9-46ea-915c-93a8d8b2477b">IGPMDomain2</a>
 

 

