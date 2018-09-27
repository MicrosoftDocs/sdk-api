---
UID: NF:wmsecure.WMCreateSecureChannel
title: WMCreateSecureChannel function
author: windows-sdk-content
description: Creates an object that implements IWMSecureChannel.
old-location: wmformat\wmcreatesecurechannel.htm
tech.root: wmformat
ms.assetid: 0893162d-f110-472a-91c0-70ba58943a22
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: WMCreateSecureChannel, WMCreateSecureChannel function [windows Media Format], wmformat.wmcreatesecurechannel, wmsecure/WMCreateSecureChannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - WMCreateSecureChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WMCreateSecureChannel function


## -description


Creates an object that implements <a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>.


## -parameters




### -param ppChannel

Address of a pointer to the <a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a> interface of the newly created secure channel object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>
 

 

