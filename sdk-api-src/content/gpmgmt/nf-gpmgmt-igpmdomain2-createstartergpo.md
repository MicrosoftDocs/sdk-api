---
UID: NF:gpmgmt.IGPMDomain2.CreateStarterGPO
title: IGPMDomain2::CreateStarterGPO
author: windows-sdk-content
description: Creates and retrieves a GPMStarterGPO object.
old-location: gpmc\igpmdomain2_createstartergpo.htm
tech.root: gpmc
ms.assetid: 652ac85b-f488-4e27-81dd-1ffc5f9f42d6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CreateStarterGPO, CreateStarterGPO method [GPMC], CreateStarterGPO method [GPMC],IGPMDomain2 interface, IGPMDomain2 interface [GPMC],CreateStarterGPO method, IGPMDomain2.CreateStarterGPO, IGPMDomain2::CreateStarterGPO, gpmc.igpmdomain2_createstartergpo, gpmgmt/IGPMDomain2::CreateStarterGPO
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gpmgmt.dll
api_name:
 - IGPMDomain2.CreateStarterGPO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMDomain2::CreateStarterGPO


## -description


Creates and retrieves a 
<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object that has a default display name and description. Typically, the caller sets the display name and description immediately after calling this method. The Starter Group Policy object (GPO) ID is generated automatically.


## -parameters




### -param ppnewTemplate [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> interface.


## -returns



<h3>C++</h3>
 Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.



<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a>  object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a>  object.




## -see-also




<a href="https://msdn.microsoft.com/5abfea14-0cb9-46ea-915c-93a8d8b2477b">IGPMDomain2</a>
 

 

