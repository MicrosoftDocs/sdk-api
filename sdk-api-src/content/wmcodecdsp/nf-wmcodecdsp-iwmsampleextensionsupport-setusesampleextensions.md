---
UID: NF:wmcodecdsp.IWMSampleExtensionSupport.SetUseSampleExtensions
title: IWMSampleExtensionSupport::SetUseSampleExtensions (wmcodecdsp.h)
description: Configures whether the codec supports sample extensions.
old-location: mf\iwmsampleextensionsupportsetusesampleextensions.htm
tech.root: medfound
ms.assetid: e268167e-4c29-45ec-9ce3-733374268113
ms.date: 12/05/2018
ms.keywords: IWMSampleExtensionSupport interface [Media Foundation],SetUseSampleExtensions method, IWMSampleExtensionSupport.SetUseSampleExtensions, IWMSampleExtensionSupport::SetUseSampleExtensions, SetUseSampleExtensions, SetUseSampleExtensions method [Media Foundation], SetUseSampleExtensions method [Media Foundation],IWMSampleExtensionSupport interface, codecapi.iwmsampleextensionsupportsetusesampleextensions, mf.iwmsampleextensionsupportsetusesampleextensions, wmcodecdsp/IWMSampleExtensionSupport::SetUseSampleExtensions
ms.topic: method
f1_keywords:
- wmcodecdsp/IWMSampleExtensionSupport.SetUseSampleExtensions
dev_langs:
- c++
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- COM
api_location:
- wmcodecdsp.h
api_name:
- IWMSampleExtensionSupport.SetUseSampleExtensions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSampleExtensionSupport::SetUseSampleExtensions


## -description


Configures whether the codec supports sample extensions.



## -parameters




### -param fUseExtensions [in]

Flag, true indicating to use extensions.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmsampleextensionsupport">IWMSampleExtensionSupport Interface</a>
 

 

