---
UID: NE:authif._RADIUS_AUTHENTICATION_PROVIDER
title: "_RADIUS_AUTHENTICATION_PROVIDER"
author: windows-sdk-content
description: The RADIUS_AUTHENTICATION_PROVIDER type enumerates the possible authentication providers that NPS can use.
old-location: nps\IAS_radius_authentication_provider.htm
tech.root: Nps
ms.assetid: 017c31f1-1654-4312-a1f0-747ea82391e1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RADIUS_AUTHENTICATION_PROVIDER, RADIUS_AUTHENTICATION_PROVIDER enumeration [Network Policy Server], _RADIUS_AUTHENTICATION_PROVIDER, _ias_radius_authentication_provider, authif/RADIUS_AUTHENTICATION_PROVIDER, authif/rapMCIS, authif/rapNone, authif/rapODBC, authif/rapProxy, authif/rapUnknown, authif/rapUsersFile, authif/rapWindowsNT, ias.radius_authentication_provider, nps.IAS_radius_authentication_provider, rapMCIS, rapNone, rapODBC, rapProxy, rapUnknown, rapUsersFile, rapWindowsNT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_AUTHENTICATION_PROVIDER
product: Windows
targetos: Windows
req.typenames: RADIUS_AUTHENTICATION_PROVIDER
req.redist: 
---

# _RADIUS_AUTHENTICATION_PROVIDER enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RADIUS_AUTHENTICATION_PROVIDER</b> type enumerates the possible authentication providers that NPS can use.


## -enum-fields




### -field rapUnknown

The authentication provider is unknown.


### -field rapUsersFile

A users' file  provides the authentication information.


### -field rapProxy

Authentication is provided by a RADIUS proxy server.


### -field rapWindowsNT

Authentication is provided by Windows Domain Authentication.


### -field rapMCIS

Authentication is provided by a Microsoft Commercial Internet System (MCIS) database.


### -field rapODBC

Authentication is provided by an Open Database Connectivity (ODBC) compliant database.


### -field rapNone

Access is unauthenticated.


## -remarks



The <b>ratProvider</b> extended attribute in 
<a href="https://msdn.microsoft.com/b0b39062-0622-48f8-a06a-232713ec8c3c">RADIUS_ATTRIBUTE_TYPE</a> uses values from the 
<b>RADIUS_AUTHENTICATION_PROVIDER</b> enumeration type.




## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/6bf9c421-f0f6-4c75-bb4d-dbe91dcb8d01">NPS Extensions Enumerations</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/b0b39062-0622-48f8-a06a-232713ec8c3c">RADIUS_ATTRIBUTE_TYPE</a>
 

 

