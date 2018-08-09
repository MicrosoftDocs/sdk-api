---
UID: NS:appmgmt._INSTALLDATA
title: "_INSTALLDATA"
author: windows-sdk-content
description: The INSTALLDATA structure specifies a group-policy application to be installed by InstallApplication.
old-location: policy\installdata_str.htm
old-project: Policy
ms.assetid: 0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PINSTALLDATA, INSTALLDATA, INSTALLDATA structure [Group Policy], PINSTALLDATA, PINSTALLDATA structure pointer [Group Policy], _INSTALLDATA, appmgmt/INSTALLDATA, appmgmt/PINSTALLDATA, policy.installdata_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: appmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: INSTALLDATA, *PINSTALLDATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Appmgmt.h
api_name:
 - INSTALLDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _INSTALLDATA structure


## -description


The <b>INSTALLDATA</b> structure specifies a group-policy application to  be installed by <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>.


## -struct-fields




### -field Type

Defines  how <b>Spec</b> specifies the application to <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>.     <b>Type</b> can be  one of the <a href="https://msdn.microsoft.com/9e62a22d-cae7-4b3e-9000-71eddb1f3cad">INSTALLSPECTYPE</a> enumeration values. Set <b>Type</b> to APPNAME to install an application specified by its user-friendly name and GPO GUID. Set <b>Type</b> to FILEEXT to install  an application specified by its file name extension.


### -field Spec

An <a href="https://msdn.microsoft.com/e9c1b943-9cb0-480f-8ab7-0f439087216a">INSTALLSPEC</a> structure that specifies the application.


## -see-also




<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>



<a href="https://msdn.microsoft.com/e9c1b943-9cb0-480f-8ab7-0f439087216a">INSTALLSPEC</a>



<a href="https://msdn.microsoft.com/9e62a22d-cae7-4b3e-9000-71eddb1f3cad">INSTALLSPECTYPE</a>



<a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>



<a href="https://msdn.microsoft.com/d45494e2-d86e-4d94-a158-4024eacf46a2">UninstallApplication</a>
 

 

