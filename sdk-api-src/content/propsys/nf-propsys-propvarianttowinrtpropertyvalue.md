---
UID: NF:propsys.PropVariantToWinRTPropertyValue
title: PropVariantToWinRTPropertyValue function
author: windows-sdk-content
description: Extracts data from a PROPVARIANT structure into a Windows Runtime property value.
old-location: properties\propvarianttowinrtpropertyvalue.htm
tech.root: properties
ms.assetid: 38DD3673-17FD-4F2A-BA58-A1A9983B92BF
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropVariantToWinRTPropertyValue, PropVariantToWinRTPropertyValue function [Windows Properties], properties.propvarianttowinrtpropertyvalue, propsys/PropVariantToWinRTPropertyValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propsys.h
req.include-header: Windows.Foundation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PropVariantToWinRTPropertyValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropVariantToWinRTPropertyValue function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into a Windows Runtime property value. Note that in some cases more than one <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> type maps to a single Windows Runtime property type.


## -parameters




### -param propvar [in]

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param riid [in]

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IPropertyValue (defined in Windows.Foundation.h).


### -param ppv [out]

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="http://go.microsoft.com/fwlink/p/?LinkID=313209">IPropertyValue</a> pointer. If the call fails, this value is <b>NULL</b>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We recommend that you use the <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=313206">PropertyValue class</a>
 

 

