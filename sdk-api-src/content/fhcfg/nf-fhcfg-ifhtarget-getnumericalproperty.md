---
UID: NF:fhcfg.IFhTarget.GetNumericalProperty
title: IFhTarget::GetNumericalProperty (fhcfg.h)
author: windows-sdk-content
description: Retrieves a numeric property of the File History backup target that is represented by an IFhTarget interface.
old-location: winprog\ifhtarget_getnumericalproperty.htm
tech.root: DevNotes
ms.assetid: 3FA2F3AB-A406-4F19-AA5A-0D5596F1BF2C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNumericalProperty, GetNumericalProperty method [Windows API], GetNumericalProperty method [Windows API],IFhTarget interface, IFhTarget interface [Windows API],GetNumericalProperty method, IFhTarget.GetNumericalProperty, IFhTarget::GetNumericalProperty, fhcfg/IFhTarget::GetNumericalProperty, winprog.ifhtarget_getnumericalproperty
ms.topic: method
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - Fhcfg.h
api_name:
 - IFhTarget.GetNumericalProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFhTarget::GetNumericalProperty


## -description


Retrieves a numeric property of the File History backup target that is represented by an <a href="https://msdn.microsoft.com/5A73A81A-72A3-4794-86E5-9CA8FCA200C0">IFhTarget</a> interface.


## -parameters




### -param PropertyType [in]

Specifies the numeric property. See the <a href="https://msdn.microsoft.com/0A39626B-942F-4BD6-930D-15E9D401F0FF">FH_TARGET_PROPERTY_TYPE</a> enumeration for a list of possible numeric properties.


### -param PropertyValue [out]

Receives the value of the numeric property.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.




## -remarks



The <a href="https://msdn.microsoft.com/0A39626B-942F-4BD6-930D-15E9D401F0FF">FH_TARGET_PROPERTY_TYPE</a> enumeration defines property types for string properties and numeric properties. However, the <b>IFhTarget::GetNumericalProperty</b> method can only be used to retrieve numeric properties. String properties must be retrieved by  calling the <a href="https://msdn.microsoft.com/DC5FE023-FA6E-4B97-AD9D-830975A17159">IFhTarget::GetStringProperty</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0A39626B-942F-4BD6-930D-15E9D401F0FF">FH_TARGET_PROPERTY_TYPE</a>



<a href="https://msdn.microsoft.com/5A73A81A-72A3-4794-86E5-9CA8FCA200C0">IFhTarget</a>



<a href="https://msdn.microsoft.com/DC5FE023-FA6E-4B97-AD9D-830975A17159">IFhTarget::GetStringProperty</a>
 

 

