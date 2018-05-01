---
UID: NS:wiamindr_lh._WIA_PROPERTY_INFO
title: "_WIA_PROPERTY_INFO"
author: windows-driver-content
description: The WIA_PROPERTY_INFO structure is used to store default access and valid value information for an item property of arbitrary type.
old-location: image\wia_property_info.htm
old-project: image
ms.assetid: 9ab9edb8-aa37-4c28-81c9-3e41751f14ed
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PWIA_PROPERTY_INFO, PWIA_PROPERTY_INFO, PWIA_PROPERTY_INFO structure pointer [Imaging Devices], WIA_PROPERTY_INFO, WIA_PROPERTY_INFO structure [Imaging Devices], _WIA_PROPERTY_INFO, image.wia_property_info, wiamindr_lh/PWIA_PROPERTY_INFO, wiamindr_lh/WIA_PROPERTY_INFO, wiastrct_6e0091b3-43a3-473b-88e4-ec41533a5b0e.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: WIA_PROPERTY_INFO, *PWIA_PROPERTY_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiamindr_lh.h
api_name:
-	WIA_PROPERTY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WIA_PROPERTY_INFO structure


## -description


The WIA_PROPERTY_INFO structure is used to store default access and valid value information for an item property of arbitrary type.


## -struct-fields




### -field ValidVal


### -field ValidVal.Range

Is a structure that is filled when the property's valid values are specified by a range of integer values. This structure contains the following members:

<b>Min</b>, which indicates the minimum value of the property.

<b>Max</b>, which indicates the maximum value of the property.

<b>Nom</b>, which indicates the property's nominal value.

<b>Inc</b>, which indicates the increment value that can be used.


### -field ValidVal.Range.Min

 


### -field ValidVal.Range.Nom

 


### -field ValidVal.Range.Max

 


### -field ValidVal.Range.Inc

 


### -field ValidVal.RangeFloat

Is a structure that is filled when the property's valid values are specified by a range of floating-point values and the property type is a <b>float</b> or <b>double</b>. This structure contains the following members:

<b>Min</b>, which indicates the minimum value of the property.

<b>Max</b>, which indicates the maximum value of the property.

<b>Nom</b>, which indicates the property's nominal value.

<b>Inc</b>, which indicates the increment value that can be used. 


### -field ValidVal.RangeFloat.Min

 


### -field ValidVal.RangeFloat.Nom

 


### -field ValidVal.RangeFloat.Max

 


### -field ValidVal.RangeFloat.Inc

 


### -field ValidVal.List

Is a structure that is filled when the property's valid values are specified by a list of integer values. This structure contains the following members:

<b>cNumList</b>, which indicates the number of elements in the array of valid values to which <b>pList</b> points.

<b>Nom</b>, which indicates the nominal value of the property.

<b>pList</b>, which is an array of valid values the property can be set to.


### -field ValidVal.List.cNumList

 


### -field ValidVal.List.Nom

 


### -field ValidVal.List.pList

 


### -field ValidVal.ListFloat

Is a structure that is filled when the property's valid values are specified by a list of floating-point values. This structure contains the following members:

<b>cNumList</b>, which indicates the number of elements in the array of valid values to which <b>pList</b> points.

<b>Nom</b>, which indicates the nominal value of the property.

<b>pList</b>, which is an array of valid values the property can be set to.


### -field ValidVal.ListFloat.cNumList

 


### -field ValidVal.ListFloat.Nom

 


### -field ValidVal.ListFloat.pList

 


### -field ValidVal.ListGuid

Is a structure that is filled when the property's valid values are specified by a list of GUIDs. This structure contains the following members:

<b>cNumList</b>, which indicates the number of elements in the array of valid values to which <b>pList</b> points.

<b>Nom</b>, which indicates the nominal value of the property.

<b>pList</b>, which is an array of valid values the property can be set to. 


### -field ValidVal.ListGuid.cNumList

 


### -field ValidVal.ListGuid.Nom

 


### -field ValidVal.ListGuid.pList

 


### -field ValidVal.ListBStr

Is a structure that is filled when the property's valid values are specified by a list of strings. This structure contains the following members:

<b>cNumList</b>, which indicates the number of elements in the array of valid values to which <b>pList</b> points.

<b>Nom</b>, which indicates the nominal value of the property.

<b>pList</b>, which is an array of valid values the property can be set to.


### -field ValidVal.ListBStr.cNumList

 


### -field ValidVal.ListBStr.Nom

 


### -field ValidVal.ListBStr.pList

 


### -field ValidVal.Flag

Is a structure that is filled when the property's valid values are specified by a bitset of flags. This structure contains the following members:

<b>Nom</b>, which indicates the nominal value of the property.

<b>ValidBits</b>, which is a mask indicating which bit values can be set. This member should be a bitwise OR of all possible user-defined flag values.


### -field ValidVal.Flag.Nom

 


### -field ValidVal.Flag.ValidBits

 


### -field ValidVal.None

Is a structure that is filled when the property's valid values are not given in a list, range, or bitset. This structure contains a member named <b>Dummy</b>, which indicates the property is of type NONE. 


### -field ValidVal.None.Dummy

 


### -field lAccessFlags

Specifies the access and property attribute flags for a property. See the Microsoft Windows SDK documentation for a list of WIA property attribute flags. 


### -field vt

Specifies the variant data type for the property. This member, which can be one of the following, controls which structure member of the <b>ValidValunion</b> is valid:

VT_UI1

VT_UI2

VT_UI4

VT_I2

VT_I4

VT_R4

VT_R8

VT_CLSID

VT_BSTR

See PROPVARIANT in the Windows SDK documentation for more information.


## -remarks



The WIA_PROPERTY_INFO is used by the minidriver to store information about a property of arbitrary type. This structure is also used by the <b>wiasSetItemPropAttribs</b> to set a property's valid values. The <b>lAccessFlags</b> member controls whether access to a property is read-only or read/write. This member also conveys information about the set of valid values for a property when they are defined by a list of values, a range of values, or a bitset of flags. The <b>vt</b> member contains information about the type of the property. Both members should be used to determine which member of the <b>ValidValunion</b> can be accessed. 

For example, for a read/write property of type <b>long</b>, whose valid values are integers in the range -128 to 127, and whose nominal value is 0, <b>lAccessFlags</b> would be set to WIA_PROP_RW | WIA_PROP_RANGE, and <b>vt</b> would be set to VT_I4. <b>Range.Min</b> would be set to -128, <b>Range.Max</b> would be set to 127, and <b>Range.Inc</b> would be set to 1. <b>Range.Nom</b> would be set to 0.

For a different property whose valid values are defined by a list of three GUID values, <b>lAccessFlags</b> would have its WIA_PROP_LIST bit set, and <b>vt</b> would be set to VT_CLSID. <b>ListGuid.cNumList</b> would be set to 3, and the three GUIDs are <b>ListGuid.pList</b>[0], <b>ListGuid.pList</b>[1], and <b>ListGuid.pList</b>[2].

A property whose valid values are defined by a bitset of the values 0x01, 0x02, 0x04, and 0x08 would have the WIA_PROP_FLAG bit set in <b>lAccessFlags</b>, and <b>vt</b> would be set to VT_UI4. For such a property, the value stored in <b>Flag.ValidBits</b> would be 0x0F, the bitwise OR of the four flag values previously mentioned.

The following examples show how to use array data with WIA_PROPERTY_INFO and how to call <a href="https://msdn.microsoft.com/library/windows/hardware/ff549475">wiasWriteMultiple</a> to set your property values.

Initialization might look like the following example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>  // Initialize WIA_IPA_ITEM_TIME (NONE)
  g_pszItemDefaults[13]              = WIA_IPA_ITEM_TIME_STR;
  g_piItemDefaults [13]              = WIA_IPA_ITEM_TIME;
  g_pvItemDefaults [13].cai.celems   = MyNumberOfElements;
  g_pvItemDefaults [13].cai.pelems   = PointerToMyArray;
  g_pvItemDefaults [13].vt           = VT_VECTOR|VT_UI2; // MyArray is an array of DWORD values
  g_psItemDefaults [13].ulKind       = PRSPEC_PROPID;
  g_psItemDefaults [13].propid       = g_piItemDefaults [13];
  g_wpiItemDefaults[13].lAccessFlags = WIA_PROP_READ|WIA_PROP_NONE;
  g_wpiItemDefaults[13].vt           = g_pvItemDefaults [13].vt;</pre>
</td>
</tr>
</table></span></div>
At run time, changing the value with <b>wiasWriteMultiple</b> might look like the following example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>  PROPVARIANT propVar;
  PROPSPEC    propSpec;
  PropVariantInit(&amp;propVar);
  propVar.vt          = VT_VECTOR | VT_UI2;
  propVar.caui.cElems = sizeof(SYSTEMTIME) / sizeof(WORD);
  propVar.caui.pElems = (WORD *) &amp;CurrentTimeStruct;
  propSpec.ulKind     = PRSPEC_PROPID;
  propSpec.propid     = WIA_IPA_ITEM_TIME;
  hr                  = wiasWriteMultiple(pWiasContext, 1, &amp;propSpec, &amp;propVar);</pre>
</td>
</tr>
</table></span></div>
<b>Note</b>  WIA uses the COM PROPVARIANT type, VARIANT (defined in the Microsoft Windows SDK documentation), so the default is VT_VECTOR, and not VT_ARRAY (which is also supported).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549358">wiasSetItemPropAttribs</a>
 

 

