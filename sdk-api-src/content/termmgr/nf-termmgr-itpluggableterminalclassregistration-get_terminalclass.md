---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_TerminalClass
title: ITPluggableTerminalClassRegistration::get_TerminalClass
author: windows-sdk-content
description: The get_TerminalClass method gets the terminal's terminal class.
old-location: tapi3\itpluggableterminalclassregistration_get_terminalclass.htm
old-project: Tapi
ms.assetid: 8da33c46-a369-4501-8249-48ad5d454c58
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_TerminalClass method, ITPluggableTerminalClassRegistration.get_TerminalClass, ITPluggableTerminalClassRegistration::get_TerminalClass, _tapi3_itpluggableterminalclassregistration_get_terminalclass, get_TerminalClass, get_TerminalClass method [TAPI 2.2], get_TerminalClass method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_terminalclass, termmgr/ITPluggableTerminalClassRegistration::get_TerminalClass
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalClassRegistration.get_TerminalClass
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalClassRegistration::get_TerminalClass


## -description


The 
<b>get_TerminalClass</b> method gets the terminal's terminal class.


## -parameters




### -param pTerminalClass [out]

The <b>BSTR</b> representation of the 
<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">terminal class</a>. The <b>BSTR</b> is allocated using 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>



<a href="https://msdn.microsoft.com/257adef8-f578-4c8c-9fe9-df59572b7f6e">put_TerminalClass</a>
 

 

