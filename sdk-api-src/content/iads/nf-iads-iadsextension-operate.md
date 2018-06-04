---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

