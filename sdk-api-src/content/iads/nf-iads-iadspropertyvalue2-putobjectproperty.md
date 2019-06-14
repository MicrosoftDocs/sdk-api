---
UID: NF:iads.IADsPropertyValue2.PutObjectProperty
title: IADsPropertyValue2::PutObjectProperty (iads.h)
author: windows-sdk-content
description: Sets an attribute value.
old-location: adsi\iadspropertyvalue2_putobjectproperty.htm
tech.root: adsi
ms.assetid: 53dad13f-7df7-4c1d-8c8a-946c291b20c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsPropertyValue2 interface [ADSI],PutObjectProperty method, IADsPropertyValue2.PutObjectProperty, IADsPropertyValue2::PutObjectProperty, PutObjectProperty, PutObjectProperty method [ADSI], PutObjectProperty method [ADSI],IADsPropertyValue2 interface, _ds_iadspropertyvalue2_putobjectproperty, adsi.iadspropertyvalue2__putobjectproperty, adsi.iadspropertyvalue2_putobjectproperty, iads/IADsPropertyValue2::PutObjectProperty
ms.topic: method
req.header: iads.h
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPropertyValue2.PutObjectProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsPropertyValue2::PutObjectProperty


## -description


The <b>IADsPropertyValue2::PutObjectProperty</b> method sets an attribute value.


## -parameters




### -param lnADsType [in]

Contains one of the <a href="https://docs.microsoft.com/windows/desktop/api/iads/ne-iads-__midl___midl_itf_ads_0000_0000_0001">ADSTYPEENUM</a> values that specifies the data format of the value set. This value must correspond to the <i>pvProp</i> variant type. For more information and a list of the <i>lnADsType</i> values and corresponding <i>pvProp</i> variant types, see <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadspropertyvalue2">IADsPropertyValue2</a>.


### -param vProp [in]

Pointer to a <b>VARIANT</b> that contains the new attribute value. The variant type of this data must correspond to the value in <i>lnADsType</i>. For more information and a list of the <i>lnADsType</i> values and corresponding <i>pvProp</i> variant types, see <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadspropertyvalue2">IADsPropertyValue2</a>.


## -returns



Returns <b>S_OK</b> if successful or an error code otherwise. The following are the most common error codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/ne-iads-__midl___midl_itf_ads_0000_0000_0001">ADSTYPEENUM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadspropertyvalue">IADsPropertyValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadspropertyvalue2">IADsPropertyValue2</a>
 

 

