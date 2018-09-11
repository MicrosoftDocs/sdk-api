---
UID: NF:gpmgmt.IGPMDomain2.GetStarterGPO
title: IGPMDomain2::GetStarterGPO
author: windows-sdk-content
description: Retrieves a GPMStarterGPO object that has a specified Group Policy object ID.
old-location: gpmc\igpmdomain2_getstartergpo.htm
tech.root: GPMC
ms.assetid: 0648c653-94da-40d6-98c2-46f80a51bc90
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetStarterGPO, GetStarterGPO method [GPMC], GetStarterGPO method [GPMC],IGPMDomain2 interface, IGPMDomain2 interface [GPMC],GetStarterGPO method, IGPMDomain2.GetStarterGPO, IGPMDomain2::GetStarterGPO, gpmc.igpmdomain2_getstartergpo, gpmgmt/IGPMDomain2::GetStarterGPO
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
 - IGPMDomain2.GetStarterGPO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMDomain2::GetStarterGPO


## -description


Retrieves a 
<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object that has a specified Group Policy object ID. The GPO ID is represented by a GUID.


## -parameters




### -param bstrGuid [in]

Required. GUID that represents the ID of the GPO to access. Use a null-terminated string.


### -param ppTemplate [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMStarterGPO</a> interface for the specified Starter GPO ID.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> object.




## -see-also




<a href="https://msdn.microsoft.com/5abfea14-0cb9-46ea-915c-93a8d8b2477b">IGPMDomain2</a>
 

 

