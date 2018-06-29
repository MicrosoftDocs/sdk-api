---
UID: NF:gpmgmt.IGPM.InitializeReporting
title: IGPM::InitializeReporting
author: windows-sdk-content
description: The InitializeReporting method sets the location to search for .adm files. This method initializes reporting in an asynchronous manner.
old-location: gpmc\igpm_initializereporting.htm
old-project: GPMC
ms.assetid: 6e9f6ac5-d6d7-4360-b722-0b22e2391d20
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GPM object [GPMC],InitializeReporting method, IGPM interface [GPMC],InitializeReporting method, IGPM.InitializeReporting, IGPM::InitializeReporting, InitializeReporting, InitializeReporting method [GPMC], InitializeReporting method [GPMC],GPM object, InitializeReporting method [GPMC],IGPM interface, gpmc.igpm_initializereporting, gpmgmt/IGPM::InitializeReporting
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
 - IGPM.InitializeReporting
 - GPM.InitializeReporting
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPM::InitializeReporting


## -description


The <b>InitializeReporting</b> method sets the location to search for .adm files. This method initializes reporting in an asynchronous manner.

For both Group Policy object (GPO) reporting or Resultant Set of Policy (RSOP) reporting, the Group Policy Management Console (GPMC) searches for and loads .adm files in the following order. First it searches for the specified .adm files in the specified location. Then it searches for any additional .adm files in the default location. Finally it searches  the GPO or RSoP for any additional .adm files.


## -parameters




### -param bstrAdmPath [in]

Location to search for .adm files. Use a null-terminated string.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>
 

 

