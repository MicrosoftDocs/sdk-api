---
UID: NF:lowlevelmonitorconfigurationapi.GetCapabilitiesStringLength
title: GetCapabilitiesStringLength function (lowlevelmonitorconfigurationapi.h)
description: Retrieves the length of a monitor's capabilities string.helpviewer_keywords: ["GetCapabilitiesStringLength","GetCapabilitiesStringLength function [Monitor Configuration]","lowlevelmonitorconfigurationapi/GetCapabilitiesStringLength","monitor.getcapabilitiesstringlength"]
old-location: monitor\getcapabilitiesstringlength.htm
tech.root: Monitor
ms.assetid: fe38e63d-b5b8-4b64-b7cb-9ff1c20a2e4a
ms.date: 12/05/2018
ms.keywords: GetCapabilitiesStringLength, GetCapabilitiesStringLength function [Monitor Configuration], lowlevelmonitorconfigurationapi/GetCapabilitiesStringLength, monitor.getcapabilitiesstringlength
f1_keywords:
- lowlevelmonitorconfigurationapi/GetCapabilitiesStringLength
dev_langs:
- c++
req.header: lowlevelmonitorconfigurationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- dxva2.dll
api_name:
- GetCapabilitiesStringLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCapabilitiesStringLength function


## -description


Retrieves the length of a monitor's capabilities string.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pdwCapabilitiesStringLengthInCharacters [out]

Receives the length of the capabilities string, in characters, including the terminating null character.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
          




## -remarks



This function usually returns quickly, but sometimes it can take several seconds to complete.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lowlevelmonitorconfigurationapi/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply">CapabilitiesRequestAndCapabilitiesReply</a>



<a href="https://docs.microsoft.com/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
 

 

