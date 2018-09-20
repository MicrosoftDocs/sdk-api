---
UID: NF:tapi3if.ITPluggableTerminalSuperclassInfo.get_CLSID
title: ITPluggableTerminalSuperclassInfo::get_CLSID
author: windows-sdk-content
description: The get_CLSID method gets the CLSID used to CoCreateInstance the terminal.
old-location: tapi3\itpluggableterminalsuperclassinfo_get_clsid.htm
tech.root: TAPI
ms.assetid: 96f2fc11-43b0-4082-ab3d-d5813cd55ee2
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITPluggableTerminalSuperclassInfo interface [TAPI 2.2],get_CLSID method, ITPluggableTerminalSuperclassInfo.get_CLSID, ITPluggableTerminalSuperclassInfo::get_CLSID, _tapi3_itpluggableterminalsuperclassinfo_get_clsid, get_CLSID, get_CLSID method [TAPI 2.2], get_CLSID method [TAPI 2.2],ITPluggableTerminalSuperclassInfo interface, tapi3.itpluggableterminalsuperclassinfo_get_clsid, tapi3if/ITPluggableTerminalSuperclassInfo::get_CLSID
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITPluggableTerminalSuperclassInfo.get_CLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalSuperclassInfo::get_CLSID


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




<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a>
 

 

