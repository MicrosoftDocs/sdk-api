---
UID: NF:tapi3if.ITPluggableTerminalSuperclassInfo.get_Name
title: ITPluggableTerminalSuperclassInfo::get_Name
author: windows-sdk-content
description: The get_Name method gets the terminal's friendly name.
old-location: tapi3\itpluggableterminalsuperclassinfo_get_name.htm
old-project: tapi
ms.assetid: 36f1f8a9-5bde-43ea-a68a-15ea7d9415aa
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITPluggableTerminalSuperclassInfo interface [TAPI 2.2],get_Name method, ITPluggableTerminalSuperclassInfo.get_Name, ITPluggableTerminalSuperclassInfo::get_Name, _tapi3_itpluggableterminalsuperclassinfo_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITPluggableTerminalSuperclassInfo interface, tapi3.itpluggableterminalsuperclassinfo_get_name, tapi3if/ITPluggableTerminalSuperclassInfo::get_Name
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
 - ITPluggableTerminalSuperclassInfo.get_Name
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalSuperclassInfo::get_Name


## -description


The 
<b>get_Name</b> method gets the terminal's friendly name.


## -parameters




### -param pName [out]

The <b>BSTR</b> representation of the friendly name. The <b>BSTR</b> is allocated using 
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a>
 

 

