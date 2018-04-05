---
UID: NF:strmif.IAMExtTransport.GetEditProperty
title: IAMExtTransport::GetEditProperty method
author: windows-driver-content
description: The GetEditProperty method retrieves parameters and values associated with an edit event.
old-location: dshow\iamexttransport_geteditproperty.htm
old-project: DirectShow
ms.assetid: c36b1fb1-f0a7-49df-8a6c-fb90ab268b23
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetEditProperty method [DirectShow], GetEditProperty method [DirectShow], IAMExtTransport interface, GetEditProperty,IAMExtTransport.GetEditProperty, IAMExtTransport, IAMExtTransport interface [DirectShow], GetEditProperty method, IAMExtTransport::GetEditProperty, IAMExtTransportGetEditProperty, dshow.iamexttransport_geteditproperty, strmif/IAMExtTransport::GetEditProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMExtTransport.GetEditProperty
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::GetEditProperty method


## -description



The <code>GetEditProperty</code> method retrieves parameters and values associated with an edit event.



This method is not implemented.


## -parameters




### -param EditID [in]

Specifies the edit property set. Use the identifier returned by the <a href="https://msdn.microsoft.com/40695c7c-7381-44c0-b41f-7c838c9c83b5">IAMExtTransport::SetEditPropertySet</a> method.


### -param Param [in]

Specifies the edit event parameter to retrieve.


### -param pValue [out]

pointer to a variable that receives the parameter value.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



For a list of edit event parameters and their possible values, see <a href="https://msdn.microsoft.com/85ac14c7-7b47-4462-98ba-68a73f4c7497">IAMExtTransport::SetEditProperty</a>. In addition, this method supports ED_EDIT_TEST, which determines whether the device can perform the edit. If the device filter estimates that the device can perform the edit, it returns the value OATRUE in the <i>pValue</i> parameter. If not, it returns the value OAFALSE.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/85ac14c7-7b47-4462-98ba-68a73f4c7497">IAMExtTransport::SetEditProperty</a>
 

 

