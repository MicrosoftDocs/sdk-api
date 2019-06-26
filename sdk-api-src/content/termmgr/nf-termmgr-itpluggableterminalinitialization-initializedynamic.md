---
UID: NF:termmgr.ITPluggableTerminalInitialization.InitializeDynamic
title: ITPluggableTerminalInitialization::InitializeDynamic (termmgr.h)
author: windows-sdk-content
description: The InitializeDynamic method performs primary terminal object creation for the pluggable terminal.
old-location: tapi3\itpluggableterminalinitialization_initializedynamic.htm
tech.root: Tapi
ms.assetid: 4cda6540-0c27-4234-8b7e-ffff117903b8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalInitialization interface [TAPI 2.2],InitializeDynamic method, ITPluggableTerminalInitialization.InitializeDynamic, ITPluggableTerminalInitialization::InitializeDynamic, InitializeDynamic, InitializeDynamic method [TAPI 2.2], InitializeDynamic method [TAPI 2.2],ITPluggableTerminalInitialization interface, _tapi3_itpluggableterminalinitialization_initializedynamic, tapi3.itpluggableterminalinitialization_initializedynamic, termmgr/ITPluggableTerminalInitialization::InitializeDynamic
ms.topic: method
f1_keywords: 
 - "termmgr/ITPluggableTerminalInitialization.InitializeDynamic"
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
 - ITPluggableTerminalInitialization.InitializeDynamic
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalInitialization::InitializeDynamic


## -description


The 
<b>InitializeDynamic</b> method performs primary terminal object creation for the pluggable terminal.


## -parameters




### -param iidTerminalClass [in]

The IID_ for the class of the terminal being initialized.


### -param dwMediaType [in]

ORed list of the media types supported by the terminal.


### -param Direction [in]

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor for the terminal.


### -param htAddress [in]

MSP handle for the address to associate with the terminal being created.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalinitialization">ITPluggableTerminalInitialization</a>
 

 

