---
UID: NN:msinkaut.IInkExtendedProperties
title: IInkExtendedProperties (msinkaut.h)
description: Represents a collection of IInkExtendedProperty objects that contain application-defined data.
helpviewer_keywords: ["IInkExtendedProperties","IInkExtendedProperties interface [Tablet PC]","IInkExtendedProperties interface [Tablet PC]","described","c7b7f40f-0c28-4848-83d6-d5db73eef998","msinkaut/IInkExtendedProperties","tablet.iinkextendedproperties"]
old-location: tablet\iinkextendedproperties.htm
tech.root: tablet
ms.assetid: c7b7f40f-0c28-4848-83d6-d5db73eef998
ms.date: 12/05/2018
ms.keywords: IInkExtendedProperties, IInkExtendedProperties interface [Tablet PC], IInkExtendedProperties interface [Tablet PC],described, c7b7f40f-0c28-4848-83d6-d5db73eef998, msinkaut/IInkExtendedProperties, tablet.iinkextendedproperties
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkExtendedProperties
 - msinkaut/IInkExtendedProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkExtendedProperties
 - IInkExtendedProperties._NewEnum
---

# IInkExtendedProperties interface


## -description

Represents a collection of <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperty">IInkExtendedProperty</a> objects that contain application-defined data.

## -inheritance

The <b>IInkExtendedProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkExtendedProperties</b> also has these types of members:

## -remarks

The extended property data is indexed by an application-specific globally unique identifier (GUID).

<div class="alert"><b>Note</b>  You cannot store an empty <b>IInkExtendedProperties</b> object. The object must contain data before it can be stored. For example, if you try to add extended properties to a stroke for later use, an exception is thrown if the extended property contains no data.</div>
<div> </div>
<b>IInkExtendedProperties</b> collections may be added to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a>, the <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a>, and the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> objects.

For more information about collections in Automation, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties">ExtendedProperties Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperty">IInkExtendedProperty Interface</a>
