---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_CLSID
title: ITPluggableTerminalClassInfo::get_CLSID
author: windows-sdk-content
description: The get_CLSID method gets the CLSID used to CoCreateInstance the terminal.
old-location: tapi3\itpluggableterminalclassinfo_get_clsid.htm
old-project: tapi
ms.assetid: 17513c0f-bc3a-474b-a9e0-ea91e2ae7fbf
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_CLSID method, ITPluggableTerminalClassInfo.get_CLSID, ITPluggableTerminalClassInfo::get_CLSID, _tapi3_itpluggableterminalclassinfo_get_clsid, get_CLSID, get_CLSID method [TAPI 2.2], get_CLSID method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_clsid, tapi3if/ITPluggableTerminalClassInfo::get_CLSID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalClassInfo.get_CLSID
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalClassInfo::get_CLSID


## -description


The 
<b>get_CLSID</b> method gets the CLSID used to <b>CoCreateInstance</b> the terminal.


## -parameters




### -param pCLSID [out]

The <b>BSTR</b> representation of the CLSID. The <b>BSTR</b> is allocated using 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a>
 

 

