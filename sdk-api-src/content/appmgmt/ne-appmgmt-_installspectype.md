---
UID: NE:appmgmt._INSTALLSPECTYPE
title: "_INSTALLSPECTYPE"
author: windows-sdk-content
description: The INSTALLSPECTYPE enumeration values define the ways a group policy application can be specified to the InstallApplication function. The values are used in the Type member of INSTALLDATA.
old-location: policy\installspectype_enum.htm
old-project: Policy
ms.assetid: 9e62a22d-cae7-4b3e-9000-71eddb1f3cad
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: APPNAME, FILEEXT, INSTALLSPECTYPE, INSTALLSPECTYPE enumeration [Group Policy], _INSTALLSPECTYPE, appmgmt/APPNAME, appmgmt/FILEEXT, appmgmt/INSTALLSPECTYPE, policy.installspectype_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: appmgmt.h
req.include-header: 
req.redist: 
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
req.typenames: INSTALLSPECTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Appmgmt.h
api_name:
 - INSTALLSPECTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: Apphelp.dll
req.irql: 
---

# _INSTALLSPECTYPE enumeration


## -description


The <b>INSTALLSPECTYPE</b> enumeration values define the ways  a group policy application can be specified to the  <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a> function. The values are used in the <b>Type</b> member of <a href="https://msdn.microsoft.com/0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c">INSTALLDATA</a>.


## -enum-fields




### -field APPNAME

This constant equals 1. The application is specified by its display name and group policy GUID.


### -field FILEEXT

The application is specified by its file name extension, for example, .jpg.


### -field PROGID


### -field COMCLASS




## -see-also




<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>



<a href="https://msdn.microsoft.com/0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c">INSTALLDATA</a>



<a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>



<a href="https://msdn.microsoft.com/d45494e2-d86e-4d94-a158-4024eacf46a2">UninstallApplication</a>
 

 

