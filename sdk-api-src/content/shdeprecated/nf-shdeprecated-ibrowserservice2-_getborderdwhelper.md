---
UID: NF:shdeprecated.IBrowserService2._GetBorderDWHelper
title: IBrowserService2::_GetBorderDWHelper
author: windows-sdk-content
description: Deprecated. A helper method for the implementation of GetBorderDW.
old-location: shell\IBrowserService2__GetBorderDWHelper.htm
tech.root: shell
ms.assetid: 44477311-61c6-48d0-bef8-349ca114a891
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_GetBorderDWHelper method, IBrowserService2._GetBorderDWHelper, IBrowserService2::_GetBorderDWHelper, _GetBorderDWHelper, _GetBorderDWHelper method [Windows Shell], _GetBorderDWHelper method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_GetBorderDWHelper, shell.IBrowserService2__GetBorderDWHelper, zone_IBrowserService2__GetBorderDWHelper
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IBrowserService2._GetBorderDWHelper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_GetBorderDWHelper


## -description


Deprecated. A helper method for the implementation of <a href="https://msdn.microsoft.com/b1c30a49-8d87-4855-acc0-5f33eabe5e8a">GetBorderDW</a>.


## -parameters




### -param punkSrc [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> that represents the object for which the border space is being requested.


### -param lprectBorder [in]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the dimensions of the available border space for the browser.


### -param bUseHmonitor [in]

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates whether to use an <b>HMONITOR</b> to determine the display. <b>TRUE</b> to use the <b>HMONITOR</b>; <b>FALSE</b> to ignore the particular display in the size determination.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



