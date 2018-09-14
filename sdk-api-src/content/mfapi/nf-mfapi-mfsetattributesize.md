---
UID: NF:mfapi.MFSetAttributeSize
title: MFSetAttributeSize function
author: windows-sdk-content
description: Sets width and height as a single 64-bit attribute value.
old-location: mf\mfsetattributesize.htm
tech.root: medfound
ms.assetid: cf7b3cfe-fdce-417d-8c0b-198d026b8768
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: MFSetAttributeSize, MFSetAttributeSize function [Media Foundation], cf7b3cfe-fdce-417d-8c0b-198d026b8768, mf.mfsetattributesize, mfapi/MFSetAttributeSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - mfapi.h
api_name:
 - MFSetAttributeSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFSetAttributeSize function


## -description


Sets width and height as a single 64-bit attribute value.
        


## -parameters




### -param pAttributes [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.
          


### -param guidKey [in]

A <b>GUID</b> that identifies the value to set. If this key already exists, the function overwrites the old value.
          


### -param unWidth [in]

The width.
          


### -param unHeight [in]

The height.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Some attributes specify a width and a height as a packed <b>UINT64</b> value. This function packs the width and height values into a single <b>UINT64</b> value.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes in Media Foundation</a>



<a href="https://msdn.microsoft.com/c74445b2-a2ec-4c77-a8bf-61a6b54cef75">MFGetAttributeSize</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

