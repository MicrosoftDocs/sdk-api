---
UID: NF:wmsecure.WMCreateSecureChannel_DES
title: WMCreateSecureChannel_DES function (wmsecure.h)
author: windows-sdk-content
description: Creates an object that implements IWMSecureChannel.
old-location: wmformat\wmcreatesecurechannel_des.htm
tech.root: wmformat
ms.assetid: d90e591f-82c0-4129-a810-8705d770dd3a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMCreateSecureChannel_DES, WMCreateSecureChannel_DES function [windows Media Format], wmformat.wmcreatesecurechannel_des, wmsecure/WMCreateSecureChannel_DES
ms.topic: function
f1_keywords: 
 - "wmsecure/WMCreateSecureChannel_DES"
req.header: wmsecure.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsecure.h
api_name:
 - WMCreateSecureChannel_DES
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCreateSecureChannel_DES function


## -description


Creates an object that implements <a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>.


## -parameters




### -param ppChannel

Address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a> interface of the newly created secure channel object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>
 

 

