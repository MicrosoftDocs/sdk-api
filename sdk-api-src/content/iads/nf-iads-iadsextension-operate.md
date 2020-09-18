---
UID: NF:iads.IADsExtension.Operate
title: IADsExtension::Operate (iads.h)
description: Interprets the control code and input parameters according to the specifications of the provider.
helpviewer_keywords: ["ADS_EXT_INITCREDENTIALS","IADsExtension interface [ADSI]","Operate method","IADsExtension.Operate","IADsExtension::Operate","Operate","Operate method [ADSI]","Operate method [ADSI]","IADsExtension interface","_ds_iadsextension_operate","adsi.iadsextension__operate","adsi.iadsextension_operate","iads/IADsExtension::Operate"]
old-location: adsi\iadsextension_operate.htm
tech.root: adsi
ms.assetid: c3cab311-6717-4d95-ad46-9da6047f84b8
ms.date: 12/05/2018
ms.keywords: ADS_EXT_INITCREDENTIALS, IADsExtension interface [ADSI],Operate method, IADsExtension.Operate, IADsExtension::Operate, Operate, Operate method [ADSI], Operate method [ADSI],IADsExtension interface, _ds_iadsextension_operate, adsi.iadsextension__operate, adsi.iadsextension_operate, iads/IADsExtension::Operate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsExtension::Operate
 - iads/IADsExtension::Operate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsExtension.Operate
---

# IADsExtension::Operate


## -description

The <b>IADsExtension::Operate</b> method is invoked by the aggregator to perform the extended functionality. The method interprets the control code and input parameters according to the specifications of the provider. For more information, see the provider documentation.

## -parameters

### -param dwCode [in]

A value of the ADSI extension control code. ADSI defines the following code value.



#### ADS_EXT_INITCREDENTIALS

Verifies user credentials in the extension object.

### -param varData1 [in]

Provider-supplied data the extension object will operate on. The value depends upon the control code value and is presently undefined.

### -param varData2 [in]

Provider-supplied data the extension object will operate on. The value depends upon the control code value and is presently undefined.

### -param varData3 [in]

Provider-supplied data the extension object will operate on. The value depends upon the control code value and is presently undefined.

## -returns

This method supports the standard return values, as well as the following:

For more information about other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The aggregator will ignore the <b>E_FAIL</b> and <b>E_NOTIMPL</b> return values.


#### Examples

The following C/C++ code example shows a generic implementation.


```cpp
STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
{
   HRESULT hr = S_OK;
   switch (dwCode) 
   {
      case ADS_EXT_INITCREDENTIALS:
      // Prompt for a credential.
      // MessageBox(NULL, "INITCRED", "ADsExt", MB_OK);

      break;
      default:
          hr = E_FAIL;
      break;
    }        
    return hr;
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsextension">IADsExtension</a>