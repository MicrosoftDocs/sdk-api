---
UID: NF:gpedit.IGPEInformation.GetRegistryKey
title: IGPEInformation::GetRegistryKey (gpedit.h)
description: The GetRegistryKey method retrieves a handle to the root of the registry key for the specified section of the GPO.
helpviewer_keywords: ["GPO_SECTION_MACHINE","GPO_SECTION_USER","GetRegistryKey","GetRegistryKey method [Group Policy]","GetRegistryKey method [Group Policy]","IGPEInformation interface","IGPEInformation interface [Group Policy]","GetRegistryKey method","IGPEInformation.GetRegistryKey","IGPEInformation::GetRegistryKey","_win32_igpeinformation_getregistrykey","gpedit/IGPEInformation::GetRegistryKey","policy.igpeinformation_getregistrykey"]
old-location: policy\igpeinformation_getregistrykey.htm
tech.root: Policy
ms.assetid: 23ccca67-6e49-44d1-b69e-e72b9095bed8
ms.date: 12/05/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_USER, GetRegistryKey, GetRegistryKey method [Group Policy], GetRegistryKey method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetRegistryKey method, IGPEInformation.GetRegistryKey, IGPEInformation::GetRegistryKey, _win32_igpeinformation_getregistrykey, gpedit/IGPEInformation::GetRegistryKey, policy.igpeinformation_getregistrykey
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPEInformation::GetRegistryKey
 - gpedit/IGPEInformation::GetRegistryKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGPEInformation.GetRegistryKey
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
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h. If registry information is not loaded, the method returns <b>E_FAIL</b>.

## -remarks

The registry handle is a handle to the root of the registry key. To get or set values in the 
Policies key, first call the 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function to open the <b>Software\Policies</b> key.

When you have finished using the registry handle, call the 
<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> function to close the handle.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a>