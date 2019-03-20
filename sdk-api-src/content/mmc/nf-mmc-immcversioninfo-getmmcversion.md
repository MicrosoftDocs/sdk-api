---
UID: NF:mmc.IMMCVersionInfo.GetMMCVersion
title: IMMCVersionInfo::GetMMCVersion (mmc.h)
author: windows-sdk-content
description: The GetMMCVersion method retrieves version information for the MMC application.
old-location: mmc\immcversioninfo_getmmcversion.htm
tech.root: mmc
ms.assetid: 64b8cdfe-e65e-48c6-bc7a-2349140867a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMMCVersion, GetMMCVersion method [MMC], GetMMCVersion method [MMC],IMMCVersionInfo interface, IMMCVersionInfo interface [MMC],GetMMCVersion method, IMMCVersionInfo.GetMMCVersion, IMMCVersionInfo::GetMMCVersion, _slate_immcversioninfo_getmmcversion, mmc.immcversioninfo_getmmcversion, mmc/IMMCVersionInfo::GetMMCVersion
ms.topic: method
req.header: mmc.h
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
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IMMCVersionInfo.GetMMCVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMMCVersionInfo::GetMMCVersion


## -description


The 
<b>GetMMCVersion</b> method retrieves version information for the MMC application.


## -parameters




### -param pVersionMajor [out]

The version major number. For example, if *<i>pVersionMajor</i> returns 2, then MMC version 2.x is running.


### -param pVersionMinor [out]

The version minor number. For example, if *<i>pVersionMinor</i> returns 0, then MMC version x.0 is running.


## -returns



If successful, the return value is S_OK. Other return values indicate an error code.




## -remarks



The 
<a href="https://msdn.microsoft.com/13cc0cef-3548-4f9f-b150-4f13be23d0ca">IMMCVersionInfo</a> interface is introduced in MMC 2.0. For instructions on how to determine the MMC version if MMC 1.x is installed, see 
<a href="https://msdn.microsoft.com/361fa3d0-504f-4638-94b0-e771eff75928">Detecting the MMC Version Number</a>.


#### Examples


```cpp
IMMCVersionInfo * pVersionInfo = NULL;
HRESULT   hr;

// Create an object of the MMCVersionInfo class.
hr = CoCreateInstance(CLSID_MMCVersionInfo,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IMMCVersionInfo,
                      (void**)&pVersionInfo);
if (S_OK != hr)
{
    // Error encountered.
    // If the system does not support MMCVersionInfo, report it.
    // This would occur if the system was running MMC 1.x.
    if (REGDB_E_CLASSNOTREG == hr)
        OutputDebugString(_T("MMCVersionInfo is not registered\n"));
    else
        // Another error was encountered.
        OutputDebugString(_T("Failed call to CoCreateInstance\n"));
}
else
{
    // Call the GetMMCVersion method.
    long lMajor, lMinor;
    hr = pVersionInfo->GetMMCVersion(&lMajor,
                                     &lMinor);
    if (S_OK != hr)
        OutputDebugString(_T("Failed call to GetMMCVersion\n"));
    else
    {
        OutputDebugString(_T("Success in GetMMCVersion\n"));
        // Use major and minor version information as required.
        // ...
    }
}
// Free the interface pointer.
if (NULL != pVersionInfo)
{
    pVersionInfo->Release();
    pVersionInfo = NULL;
}
```




