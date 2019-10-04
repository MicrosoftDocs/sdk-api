---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_Name
title: ITPluggableTerminalClassInfo::get_Name (tapi3if.h)
author: windows-sdk-content
description: The get_Name method gets the terminal's friendly name.
old-location: tapi3\itpluggableterminalclassinfo_get_name.htm
tech.root: Tapi
ms.assetid: 97bd38f3-27d8-4618-9138-bd972db9abb9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_Name method, ITPluggableTerminalClassInfo.get_Name, ITPluggableTerminalClassInfo::get_Name, _tapi3_itpluggableterminalclassinfo_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_name, tapi3if/ITPluggableTerminalClassInfo::get_Name
ms.topic: method
f1_keywords: 
 - "tapi3if/ITPluggableTerminalClassInfo.get_Name"
dev_langs:
 - c++
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
 - ITPluggableTerminalClassInfo.get_Name
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalClassInfo::get_Name


## -description


The 
<b>get_Name</b> method gets the terminal's friendly name.


## -parameters




### -param pName [out]

The <b>BSTR</b> representation of the terminal's friendly name. The <b>BSTR</b> is allocated using 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>
 

 

