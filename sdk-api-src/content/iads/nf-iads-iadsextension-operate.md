---
UID: NF:iads.IADsExtension.Operate
title: IADsExtension::Operate
author: windows-sdk-content
description: Interprets the control code and input parameters according to the specifications of the provider.
old-location: adsi\iadsextension_operate.htm
tech.root: adsi
ms.assetid: c3cab311-6717-4d95-ad46-9da6047f84b8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ADS_EXT_INITCREDENTIALS, IADsExtension interface [ADSI],Operate method, IADsExtension.Operate, IADsExtension::Operate, Operate, Operate method [ADSI], Operate method [ADSI],IADsExtension interface, _ds_iadsextension_operate, adsi.iadsextension__operate, adsi.iadsextension_operate, iads/IADsExtension::Operate
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
 - IADsExtension.Operate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The aggregator will ignore the <b>E_FAIL</b> and <b>E_NOTIMPL</b> return values.


#### Examples

The following C/C++ code example shows a generic implementation.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/05681526-2232-4341-859d-6773f7a58431">IADsExtension</a>
 

 

