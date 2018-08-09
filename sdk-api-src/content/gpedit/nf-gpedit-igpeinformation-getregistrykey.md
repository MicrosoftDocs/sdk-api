---
UID: NF:gpedit.IGPEInformation.GetRegistryKey
title: IGPEInformation::GetRegistryKey
author: windows-sdk-content
description: The GetRegistryKey method retrieves a handle to the root of the registry key for the specified section of the GPO.
old-location: policy\igpeinformation_getregistrykey.htm
old-project: Policy
ms.assetid: 23ccca67-6e49-44d1-b69e-e72b9095bed8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_USER, GetRegistryKey, GetRegistryKey method [Group Policy], GetRegistryKey method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetRegistryKey method, IGPEInformation.GetRegistryKey, IGPEInformation::GetRegistryKey, _win32_igpeinformation_getregistrykey, gpedit/IGPEInformation::GetRegistryKey, policy.igpeinformation_getregistrykey
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGPEInformation.GetRegistryKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPEInformation::GetRegistryKey


## -description


The
    <b>GetRegistryKey</b> method retrieves a handle to the root of the registry key for the specified section of the GPO.


## -parameters




### -param dwSection [in]

Specifies the GPO section. This parameter can be one of the following values.



#### GPO_SECTION_USER

User section



#### GPO_SECTION_MACHINE

Computer section


### -param hKey [out]

Receives the handle to the registry key. This handle is opened with all access rights. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h. If registry information is not loaded, the method returns <b>E_FAIL</b>.




## -remarks



The registry handle is a handle to the root of the registry key. To get or set values in the 
Policies key, first call the 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function to open the <b>Software\Policies</b> key.

When you have finished using the registry handle, call the 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function to close the handle.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/3b3e7793-fc69-43a3-a2b1-0aa36748a19b">IGPEInformation</a>
 

 

