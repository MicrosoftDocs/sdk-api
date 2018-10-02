---
UID: NF:gpedit.IGPEInformation.GetOptions
title: IGPEInformation::GetOptions
author: windows-sdk-content
description: The GetOptions method retrieves the options the user has selected for the Group Policy Object Editor.
old-location: policy\igpeinformation_getoptions.htm
tech.root: Policy
ms.assetid: 22c90ec4-b4cc-4a95-becd-29c2ce6e3c29
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetOptions, GetOptions method [Group Policy], GetOptions method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetOptions method, IGPEInformation.GetOptions, IGPEInformation::GetOptions, _win32_igpeinformation_getoptions, gpedit/IGPEInformation::GetOptions, policy.igpeinformation_getoptions
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
 - IGPEInformation.GetOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPEInformation::GetOptions


## -description


The
    <b>GetOptions</b> method retrieves the options the user has selected for the Group Policy Object Editor.


## -parameters




### -param dwOptions [out]

Receives a bitmask value representing the options the user has selected. Currently, this parameter returns only zero.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/3b3e7793-fc69-43a3-a2b1-0aa36748a19b">IGPEInformation</a>
 

 

