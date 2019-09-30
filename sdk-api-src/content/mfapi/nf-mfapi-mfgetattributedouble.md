---
UID: NF:mfapi.MFGetAttributeDouble
title: MFGetAttributeDouble function (mfapi.h)
author: windows-sdk-content
description: Returns a double value from an attribute store, or a default value if the attribute is not present.
old-location: mf\mfgetattributedouble.htm
tech.root: medfound
ms.assetid: 61a9e327-da29-45fd-8a99-e341561826af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 61a9e327-da29-45fd-8a99-e341561826af, MFGetAttributeDouble, MFGetAttributeDouble function [Media Foundation], mf.mfgetattributedouble, mfapi/MFGetAttributeDouble
ms.topic: function
f1_keywords: 
 - "mfapi/MFGetAttributeDouble"
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
 - MFGetAttributeDouble
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFGetAttributeDouble function


## -description



Returns a <b>double</b> value from an attribute store, or a default value if the attribute is not present.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.


### -param guidKey [in]

GUID that identifies which value to retrieve.


### -param fDefault [in]

Default value to return if the attribute store does not contain the specified attribute.


## -returns



Returns a <b>double</b> value.




## -remarks



This helper function queries the attribute store for the attribute specified by <i>guidKey</i>. If the attribute is not present or does not have type <b>double</b>, the function returns <i>fDefault</i>.

This function is convenient because it never returns a failure code. However, if the attribute in question does not have a meaningful default value, you should call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getdouble">IMFAttributes::GetDouble</a> and check for MF_E_ATTRIBUTENOTFOUND.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getdouble">IMFAttributes::GetDouble</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

