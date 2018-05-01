---
UID: NF:wiamdef.wiasCreatePropContext
title: wiasCreatePropContext function
author: windows-driver-content
description: The wiasCreatePropContext function allocates a property context to indicate which of an item's properties are being changed by the application.
old-location: image\wiascreatepropcontext.htm
old-project: image
ms.assetid: b820c19d-a12b-417b-a9a3-6a3d700009c0
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiascreatepropcontext, wiamdef/wiasCreatePropContext, wiasCreatePropContext, wiasCreatePropContext function [Imaging Devices], wiasFncs_08d1a910-1036-46c9-a7a2-115a86275d60.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wiaservc.dll
api_name:
-	wiasCreatePropContext
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasCreatePropContext function


## -description


The <b>wiasCreatePropContext </b>function allocates a property context to indicate which of an item's properties are being changed by the application.


## -parameters




### -param cPropSpec

Specifies the total number of PROPSPEC structures in the <i>pPropSpec</i> array.


### -param pPropSpec [in]

Pointer to the first element of an array of PROPSPEC structures identifying which properties are changing.


### -param cProps

Specifies the number of property identifiers stored in this context.


### -param pProps [in, optional]

Pointer to the first element of an array of property identifiers that indicate the properties to put into this property context.


### -param pContext [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552749">WIA_PROPERTY_CONTEXT</a> structure that contains a property context.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



This function allocates a property context and fills in its values. This function is generally used in <a href="https://msdn.microsoft.com/library/windows/hardware/ff549454">wiasValidateItemProperties</a> where the properties written by the application are validated.

Entries in the property context are identifiers for properties that either have dependents, or are themselves dependent on other properties. A context is used to mark which properties are being changed. When the property context is no longer needed, it should be freed by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff549195">wiasFreePropContext</a>.

The properties to which an application writes are specified by the <i>pPropSpec </i>array. The properties that were changed by the application, as well as any properties dependent on the changed properties, are specified by the <i>pProps</i> array. Only properties that have been changed by the application (and any dependent properties) can be specified in <i>pProps</i>. The PROPSPEC structure is defined in the Windows SDK documentation.

<div class="alert"><b>Note</b>  : The following properties are always present in WIA_PROPERTY_CONTEXT. Drivers can specify additional properties when creating a property context with wiasCreatePropContext.<dl>
<dd>
WIA_IPA_DATATYPE

</dd>
<dd>
WIA_IPA_DEPTH

</dd>
<dd>
WIA_IPS_XRES

</dd>
<dd>
WIA_IPS_XPOS

</dd>
<dd>
WIA_IPS_XEXTENT

</dd>
<dd>
WIA_IPA_PIXELS_PER_LINE

</dd>
<dd>
WIA_IPS_YRES

</dd>
<dd>
WIA_IPS_YPOS

</dd>
<dd>
WIA_IPS_YEXTENT

</dd>
<dd>
WIA_IPA_NUMBER_OF_LINES

</dd>
<dd>
WIA_IPS_CUR_INTENT

</dd>
<dd>
WIA_IPA_TYMED

</dd>
<dd>
WIA_IPA_FORMAT

</dd>
</dl>
</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552749">WIA_PROPERTY_CONTEXT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549195">wiasFreePropContext</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549454">wiasValidateItemProperties</a>
 

 

