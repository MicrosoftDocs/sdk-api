---
UID: NF:lowlevelmonitorconfigurationapi.GetCapabilitiesStringLength
title: GetCapabilitiesStringLength function
author: windows-sdk-content
description: Retrieves the length of a monitor's capabilities string.
old-location: monitor\getcapabilitiesstringlength.htm
old-project: Monitor
ms.assetid: fe38e63d-b5b8-4b64-b7cb-9ff1c20a2e4a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetCapabilitiesStringLength, GetCapabilitiesStringLength function [Monitor Configuration], lowlevelmonitorconfigurationapi/GetCapabilitiesStringLength, monitor.getcapabilitiesstringlength
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: MC_VCP_CODE_TYPE, *LPMC_VCP_CODE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	dxva2.dll
api_name:
-	GetCapabilitiesStringLength
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetCapabilitiesStringLength function


## -description



        Retrieves the length of a monitor's capabilities string.


## -parameters




### -param hMonitor [in]


            Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pdwCapabilitiesStringLengthInCharacters [out]


            Receives the length of the capabilities string, in characters, including the terminating null character.
          


## -returns




            If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks




        This function usually returns quickly, but sometimes it can take several seconds to complete.
      




## -see-also




<a href="https://msdn.microsoft.com/1e556f66-a77a-43f3-b54f-d14995d841f8">CapabilitiesRequestAndCapabilitiesReply</a>



<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

