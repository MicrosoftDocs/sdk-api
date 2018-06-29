---
UID: NF:rometadata.MetaDataGetDispenser
title: MetaDataGetDispenser function
author: windows-sdk-content
description: Creates a dispenser class.
old-location: winrt\metadatagetdispenser.htm
old-project: WinRT
ms.assetid: F540CD4F-BDFB-44F8-B3A8-BFDA9199F2B9
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: MetaDataGetDispenser, MetaDataGetDispenser function [Windows Runtime], rometadata/MetaDataGetDispenser, winrt.metadatagetdispenser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rometadata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - rometadata.dll
 - Ext-MS-Win-rometadata-dispenser-l1-1-0.dll
api_name:
 - MetaDataGetDispenser
product: Windows
targetos: Windows
req.lib: Rometadata.lib
req.dll: Rometadata.dll
req.irql: 
req.product: ADAM
---

# MetaDataGetDispenser function


## -description


 Creates a dispenser class.


## -parameters




### -param rclsid [in]

Type: <b>REFCLSID</b>

This parameter must be <b>CLSID_CorMetaDataDispenser</b>.


### -param riid [in]

Type: <b>REFIID</b>

The interface to implement. This parameter can be either <b>IID_IMetaDataDispenser</b> or <b>IID_IMetaDataDispenserEx</b>.


### -param ppv [out]

Type: <b>LPVOID*</b>

The dispenser class. The class implements <b>IMetaDataDispenser</b> or <b>IMetaDataDispenserEx.</b>


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



