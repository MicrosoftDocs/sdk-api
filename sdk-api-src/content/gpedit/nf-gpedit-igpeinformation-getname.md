---
UID: NF:gpedit.IGPEInformation.GetName
title: IGPEInformation::GetName
author: windows-sdk-content
description: The GetName method retrieves the unique name for the GPO. This value is usually a GUID.
old-location: policy\igpeinformation_getname.htm
tech.root: Policy
ms.assetid: 94112a6e-cd8a-4fb7-9c37-86a1b7713ddb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetName, GetName method [Group Policy], GetName method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetName method, IGPEInformation.GetName, IGPEInformation::GetName, _win32_igpeinformation_getname, gpedit/IGPEInformation::GetName, policy.igpeinformation_getname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpedit.h
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
req.lib: 
req.dll: Gpedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGPEInformation.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gpedit.h
: 
- IGPEInformation.GetName
: 
---

# IGPEInformation::GetName


## -description


The
    <b>GetName</b> method retrieves the unique name for the GPO. This value is usually a GUID.


## -parameters




### -param pszName [out]

Receives the GPO name.


### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To retrieve the GPO's friendly name, which is suitable for display, you can call the 
<a href="https://msdn.microsoft.com/3c1a43a5-5d16-4abc-85e0-1eeace2ee086">GetDisplayName</a> method.




## -see-also




<a href="https://msdn.microsoft.com/3c1a43a5-5d16-4abc-85e0-1eeace2ee086">GetDisplayName</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/3b3e7793-fc69-43a3-a2b1-0aa36748a19b">IGPEInformation</a>
 

 

