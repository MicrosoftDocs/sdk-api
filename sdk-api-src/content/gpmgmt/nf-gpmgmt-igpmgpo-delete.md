---
UID: NF:gpmgmt.IGPMGPO.Delete
title: IGPMGPO::Delete
author: windows-sdk-content
description: Deletes a Group Policy object (GPO) from the directory service and from the system volume folder (SYSVOL).
old-location: gpmc\igpmgpo_delete.htm
old-project: GPMC
ms.assetid: 63a29bf5-bac5-43af-87ec-01c3c2a5b3af
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: Delete, Delete method [GPMC], Delete method [GPMC],GPMGPO class, Delete method [GPMC],IGPMGPO interface, GPMGPO class [GPMC],Delete method, IGPMGPO interface [GPMC],Delete method, IGPMGPO.Delete, IGPMGPO::Delete, _win32_igpmgpo_delete, gpmc.igpmgpo_delete, gpmgmt/IGPMGPO::Delete
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
 - Gpmgmt.dll
api_name:
 - IGPMGPO.Delete
 - GPMGPO.Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMGPO::Delete


## -description


Deletes a Group Policy object (GPO) from the directory service and from the system volume folder (SYSVOL).


## -parameters






## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



This method does not delete GPO links. To delete GPO links, call the 
<a href="https://msdn.microsoft.com/6f4151a5-6c65-4257-a2f2-28f8395968ed">IGPMGPOLink::Delete</a> method.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 

