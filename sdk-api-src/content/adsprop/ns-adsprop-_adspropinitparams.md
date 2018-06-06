---
UID: NS:adsprop._ADSPROPINITPARAMS
title: "_ADSPROPINITPARAMS"
author: windows-sdk-content
description: Used with the ADsPropGetInitInfo function to obtain object data that a display specifier applies to.
old-location: ad\adspropinitparams.htm
old-project: AD
ms.assetid: cbee3515-5037-4d65-8817-4c63fe13ef5d
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PADSPROPINITPARAMS, ADSPROPINITPARAMS, ADSPROPINITPARAMS structure [Active Directory], PADSPROPINITPARAMS, PADSPROPINITPARAMS structure pointer [Active Directory], _ADSPROPINITPARAMS, _glines_adspropinitparams, ad.adspropinitparams, adsprop/ADSPROPINITPARAMS, adsprop/PADSPROPINITPARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: adsprop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADSPROPINITPARAMS, *PADSPROPINITPARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Adsprop.h
api_name:
 - ADSPROPINITPARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _ADSPROPINITPARAMS structure


## -description


The <b>ADSPROPINITPARAMS</b> structure is used with the <a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a> function to obtain object data that a display specifier applies to.


## -struct-fields




### -field dwSize

The size, in bytes, of the <b>ADSPROPINITPARAMS</b> structure. Set this value before calling <a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a>.


### -field dwFlags

Reserved.


### -field hr

Contains an <b>HRESULT</b> value that specifies the result of the bind/get operation. If this value does not equal <b>S_OK</b>, then the remaining structure members are not initialized and should be ignored.


### -field pDsObj

Pointer to an <a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a> interface that represents the directory object that the display specifier applies to. Do not release this interface.


### -field pwzCN

Pointer to a null-terminated Unicode string that contains the common name of the directory object.


### -field pWritableAttrs

Pointer to an <a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a> structure that contains attribute data for the directory object.


## -remarks



The <a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a> function allocates memory  for the <b>pwzCN</b> and <b>pWritableAttrs</b> members. This memory is freed by the system after all display specifier objects are destroyed. The reference count for the interface pointer in <b>pDsObj</b> is not incremented by calling <b>ADsPropGetInitInfo</b>, so the interface must not be released by the caller.




## -see-also




<a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a>



<a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a>



<a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a>
 

 

