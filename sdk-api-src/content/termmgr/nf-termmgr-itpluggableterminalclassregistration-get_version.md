---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_Version
title: ITPluggableTerminalClassRegistration::get_Version
author: windows-sdk-content
description: The get_Version method gets the terminal version.
old-location: tapi3\itpluggableterminalclassregistration_get_version.htm
tech.root: Tapi
ms.assetid: 2ce4345b-7d8e-4142-a4ee-df1e8b613a25
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_Version method, ITPluggableTerminalClassRegistration.get_Version, ITPluggableTerminalClassRegistration::get_Version, _tapi3_itpluggableterminalclassregistration_get_version, get_Version, get_Version method [TAPI 2.2], get_Version method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_version, termmgr/ITPluggableTerminalClassRegistration::get_Version
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: termmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalClassRegistration.get_Version
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalClassRegistration::get_Version


## -description


The 
<b>get_Version</b> method gets the terminal version.


## -parameters




### -param pVersion [out]

The <b>BSTR</b> representation of the terminal version. The <b>BSTR</b> is allocated using 
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>



<a href="https://msdn.microsoft.com/1fd659d3-869b-4055-bbd2-e567d13f239d">put_Version</a>
 

 

