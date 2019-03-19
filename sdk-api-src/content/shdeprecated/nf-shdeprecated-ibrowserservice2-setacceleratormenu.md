---
UID: NF:shdeprecated.IBrowserService2.SetAcceleratorMenu
title: IBrowserService2::SetAcceleratorMenu (shdeprecated.h)
author: windows-sdk-content
description: Deprecated. Implemented by a derived class to define menu accelerators that can be used in a call to TranslateAcceleratorSB.
old-location: shell\IBrowserService2_SetAcceleratorMenu.htm
tech.root: shell
ms.assetid: 64c7ce89-c3c5-4a09-aff2-57103ade671a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBrowserService2 interface [Windows Shell],SetAcceleratorMenu method, IBrowserService2.SetAcceleratorMenu, IBrowserService2::SetAcceleratorMenu, SetAcceleratorMenu, SetAcceleratorMenu method [Windows Shell], SetAcceleratorMenu method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::SetAcceleratorMenu, shell.IBrowserService2_SetAcceleratorMenu, zone_IBrowserService2_SetAcceleratorMenu
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2.SetAcceleratorMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::SetAcceleratorMenu


## -description


Deprecated. Implemented by a derived class to define menu accelerators that can be used in a call to <a href="https://msdn.microsoft.com/dda5c085-7199-4b83-b03e-e4c715665157">TranslateAcceleratorSB</a>.


## -parameters




### -param hacc [in]

Type: <b>HACCEL</b>

A handle to an array of <a href="https://msdn.microsoft.com/en-us/library/ms646340(v=VS.85).aspx">ACCEL</a> structures, each structure describing a keyboard mnemonic.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



