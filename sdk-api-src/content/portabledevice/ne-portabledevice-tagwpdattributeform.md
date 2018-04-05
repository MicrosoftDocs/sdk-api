---
UID: NE:portabledevice.tagWpdAttributeForm
title: tagWpdAttributeForm
author: windows-driver-content
description: The WpdAttributeForm enumeration type describes how a property stores its values.
old-location: wpdsdk\wpdattributeform.htm
old-project: wpd_sdk
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION, WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER, WPD_PROPERTY_ATTRIBUTE_FORM_RANGE, WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION, WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED, WpdAttributeForm, WpdAttributeForm enumeration [Windows Portable Devices SDK], enumeration [Windows Portable Devices SDK], portabledevice/WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION, portabledevice/WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER, portabledevice/WPD_PROPERTY_ATTRIBUTE_FORM_RANGE, portabledevice/WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION, portabledevice/WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED, portabledevice/WpdAttributeForm, tagWpdAttributeForm, wpdsdk.wpdattributeform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: portabledevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WpdAttributeForm
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WpdAttributeForm
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWpdAttributeForm enumeration


## -description



        The <b>WpdAttributeForm</b> enumeration type describes how a property stores its values.
      


## -enum-fields




### -field WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED


            The form of the property's data is not specified.
          


### -field WPD_PROPERTY_ATTRIBUTE_FORM_RANGE


            The value is expressed as a range of values, with a minimum and a maximum.
          


### -field WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION


            The property has a series of individual values.
          


### -field WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION


            The property value is a regular expression, not a literal expression.
          


### -field WPD_PROPERTY_ATTRIBUTE_FORM_OBJECT_IDENTIFIER




#### - WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER


            The property value represents an object identifier.
          


## -remarks




        This enumeration is used by the <a href="attributes.htm">WPD_PROPERTY_ATTRIBUTE_FORM</a> property to describe how a property's data is stored.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

