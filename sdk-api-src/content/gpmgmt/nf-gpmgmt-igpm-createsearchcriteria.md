---
UID: NF:gpmgmt.IGPM.CreateSearchCriteria
title: IGPM::CreateSearchCriteria
author: windows-sdk-content
description: Creates and returns a GPMSearchCriteria that represents the criteria to use for performing search operations when you use the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpm_createsearchcriteria.htm
old-project: GPMC
ms.assetid: 7bb99109-c0d6-47cb-9ea4-6c60c1607b79
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: CreateSearchCriteria, CreateSearchCriteria method [GPMC], CreateSearchCriteria method [GPMC],GPM class, CreateSearchCriteria method [GPMC],IGPM interface, GPM class [GPMC],CreateSearchCriteria method, IGPM interface [GPMC],CreateSearchCriteria method, IGPM.CreateSearchCriteria, IGPM::CreateSearchCriteria, _win32_igpm_createsearchcriteria, gpmc.igpm_createsearchcriteria, gpmgmt/IGPM::CreateSearchCriteria
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
 - IGPM.CreateSearchCriteria
 - GPM.CreateSearchCriteria
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPM::CreateSearchCriteria


## -description


Creates and returns a <a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">GPMSearchCriteria</a> that represents the criteria to use for performing search operations when you use the Group Policy Management Console (GPMC) interfaces.


## -parameters




### -param ppIGPMSearchCriteria [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSearchCriteria</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSearchCriteria</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a>
 

 

