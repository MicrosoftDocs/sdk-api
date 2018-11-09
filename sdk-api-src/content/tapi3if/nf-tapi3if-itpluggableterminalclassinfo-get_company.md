---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_Company
title: ITPluggableTerminalClassInfo::get_Company
author: windows-sdk-content
description: The get_Company method gets the name of the company that issued this pluggable terminal.
old-location: tapi3\itpluggableterminalclassinfo_get_company.htm
tech.root: tapi
ms.assetid: b5595b18-264f-437f-8533-b7c87e6e7d00
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_Company method, ITPluggableTerminalClassInfo.get_Company, ITPluggableTerminalClassInfo::get_Company, _tapi3_itpluggableterminalclassinfo_get_company, get_Company, get_Company method [TAPI 2.2], get_Company method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_company, tapi3if/ITPluggableTerminalClassInfo::get_Company
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
 - ITPluggableTerminalClassInfo.get_Company
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalClassInfo::get_Company


## -description


The 
<b>get_Company</b> method gets the name of the company that issued this pluggable terminal.


## -parameters




### -param pCompany [out]

The <b>BSTR</b> representation of the terminal's company name. The <b>BSTR</b> is allocated using 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a>
 

 

