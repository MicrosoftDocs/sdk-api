---
UID: NF:mfapi.MFCreateAttributes
title: MFCreateAttributes function
author: windows-sdk-content
description: Creates an empty attribute store.
old-location: mf\mfcreateattributes.htm
tech.root: MedFound
ms.assetid: a79b1edd-5ca1-4550-a6ce-58073155affd
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MFCreateAttributes, MFCreateAttributes function [Media Foundation], a79b1edd-5ca1-4550-a6ce-58073155affd, mf.mfcreateattributes, mfapi/MFCreateAttributes
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateAttributes function


## -description


Creates an empty attribute store.
        


## -parameters




### -param ppMFAttributes [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. The caller must release the interface.
          


### -param cInitialSize [in]

The initial number of elements allocated for the attribute store. The attribute store grows as needed.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Attributes are used throughout Microsoft Media Foundation to configure objects, describe media formats, query object properties, and other purposes. For more information, see <a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes in Media Foundation</a>.

For a complete list of all the defined attribute GUIDs in Media Foundation, see <a href="https://msdn.microsoft.com/445fc879-3c9e-409d-8d05-ecd1ff9afc19">Media Foundation Attributes</a>.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes in Media Foundation</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

