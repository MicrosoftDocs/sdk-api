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

# IADsExtension::PrivateGetIDsOfNames


## -description


The <b>IADsExtension::PrivateGetIDsOfNames</b> method is called by the aggregator, ADSI, after ADSI determines that the extension is used to support a dual or dispatch interface. The method can use the type data to get DISPID using  <a href="6f6cf233-3481-436e-8d6a-51f93bf91619">IDispatch::GetIDsOfNames</a>.


## -parameters




### -param riid

Reserved for future use. It must be IID_NULL.


### -param rgszNames

Passed-in array of names to be mapped.


### -param cNames

Count of the names to be mapped.


### -param lcid

The locale context in which to interpret the names.


### -param rgDispid

Caller-allocated array, each element of which contains an identifier that corresponds to one of the names passed in the <i>rgszNames</i> array. The first element represents the member name. The subsequent elements represent each of the member's parameters.


## -returns



The return values are the same as those of the standard <a href="6f6cf233-3481-436e-8d6a-51f93bf91619">IDispatch::GetIDsOfNames</a> method. For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



All the parameters have the same meaning as the corresponding ones in the standard <a href="6f6cf233-3481-436e-8d6a-51f93bf91619">IDispatch::GetIDsOfNames</a>(). The extension component returns a unique identifier (<i>rgDispID</i>) for each method or property defined in the supported dual interfaces. The uniqueness is enforced within the extension component. The ADSI provider must ensure the uniqueness of the DISPIDs of all extension objects and the aggregator (ADSI) itself. The <i>rgDispID</i> parameter must be between 1 and 16777215 (2^24-1), or -1 (DISPID_UNKNOWN).


#### Examples

The following C/C++ code example shows a generic implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{
  if (rgdispid == NULL)
  {
     return E_POINTER;
  }
  return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/05681526-2232-4341-859d-6773f7a58431">IADsExtension</a>



<a href="https://msdn.microsoft.com/5af74a05-df64-4679-890b-a5a031633fd8">IADsExtension::PrivateInvoke</a>



<a href="6f6cf233-3481-436e-8d6a-51f93bf91619">IDispatch::GetIDsOfNames</a>
 

 

