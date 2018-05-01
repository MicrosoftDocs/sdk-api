---
UID: NL:wiautil.CWiauPropertyList
title: CWiauPropertyList
author: windows-driver-content
description: The CWiauPropertyList class can be used to create and maintain a list of properties for a device.
old-location: image\cwiaupropertylist_class.htm
old-project: image
ms.assetid: 4f11bec0-8ff4-4fa0-824c-71ce9774d5d1
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CWiauPropertyList, CWiauPropertyList class [Imaging Devices], CWiauPropertyList class [Imaging Devices], described, image.cwiaupropertylist_class, wiauFncs_b6021ff9-9843-4f31-b2c1-aff36af0cbc6.xml, wiautil/CWiauPropertyList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: wiautil.h
req.include-header: 
req.target-type: Windows
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
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wiautil.h
api_name:
-	CWiauPropertyList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# CWiauPropertyList class


## -description


The <b>CWiauPropertyList</b> class can be used to create and maintain a list of properties for a device.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CWiauPropertyList</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>CWiauPropertyList</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b847c3e-f773-44d0-a033-3e40bc2e01fc">~CWiauPropertyList</a>
</td>
<td align="left" width="63%">
The <b>~CWiauPropertyList</b> method is the destructor for the <b>CWiauPropertyList</b> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e493d3c-81b6-4db5-a550-c86eadf5a723">CWiauPropertyList</a>
</td>
<td align="left" width="63%">
The <b>CWiauPropertyList</b> method is the constructor for the <b>CWiauPropertyList</b> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/599c97af-1285-4fb9-af0b-edcd48249692">DefineProperty</a>
</td>
<td align="left" width="63%">
The <b>DefineProperty</b> method adds a property definition to a property list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a06de368-71a1-49f1-a948-1b69ca359fb6">GetPropId</a>
</td>
<td align="left" width="63%">
The <b>GetPropId</b> method finds the property ID for a property, given its index in the property list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
The <b>Init</b> method initializes a property list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/454e51fc-f81a-49c8-9e07-e32819af2642">LookupPropId</a>
</td>
<td align="left" width="63%">
The <b>LookupPropId</b> method finds a property's index, given its property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f7d6975-4c90-4351-bf68-89786bafcc8e">SendToWia</a>
</td>
<td align="left" width="63%">
The <b>SendToWia</b> method calls the WIA service to define all of the properties currently contained in the property list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/207125d3-0833-4c5d-b66f-aa49c96a6a2d">SetAccessSubType</a>
</td>
<td align="left" width="63%">
The <b>SetAccessSubType</b> method resets a property's access and subtype.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/207125d3-0833-4c5d-b66f-aa49c96a6a2d">SetCurrentValue(BSTR)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(BSTR)</b> method sets the current value of a property of type <b>BSTR</b>, and sets its type to <b>VT_BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/017ab648-ee62-47f5-abd3-f4eac4378b8a">SetCurrentValue(BYTE*)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(BYTE*)</b> method sets the current value of a property consisting of an array of bytes, and sets its type to <b>VT_UI1</b> | <b>VT_VECTOR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0283b46-c1a2-469b-8167-f5dc63719c16">SetCurrentValue(CLSID)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(CLSID)</b> method sets the current value of a property of type <b>CLSID</b>, and sets its type to <b>VT_CLSID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfcbe65b-7da1-4427-a58f-cbec4ce355bf">SetCurrentValue(FLOAT)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(FLOAT)</b> method sets the current value of a property of type <b>FLOAT</b>, and sets its type to <b>VT_R4</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/583c8ec9-7a57-4da3-beaf-9f9db943a652">SetCurrentValue(LONG)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(LONG)</b> method sets the current value of a property of type <b>LONG</b>, and sets its type to <b>VT_I4</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1823dec6-aec8-47eb-9543-9acfd32c4b0d">SetCurrentValue(SYSTEMTIME)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(SYSTEMTIME)</b> method sets the current value of a property of type <b>SYSTEMTIME</b>, and sets its type to <b>VT_UI2</b> | <b>VT_VECTOR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b806e310-4e6d-4258-8dd5-0c9aa35a35f4">SetValidValues(BSTR, list)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(BSTR, list)</b> method sets the type, as well as default, current, and valid values for a <b>BSTR</b> property associated with a list of values. The method also sets the property type to <b>VT_BSTR</b> and subtype to <b>WIA_PROP_LIST</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d401ed85-de6b-4758-b7c4-d6fcd59c157e">SetValidValues(CLSID, list)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(CLSID, list)</b> method sets the type, as well as default, current, and valid values for a <b>CLSID</b> property associated with a list of values. The method also sets the property type to <b>VT_CLSID</b> and subtype to <b>WIA_PROP_LIST</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e61b5bbb-14a8-4dfa-af36-99c5dd1ecc99">SetValidValues(flag)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(flag)</b> method sets the type, as well as default, current, and valid values for a property whose values are defined by a flag. The method also sets the property type to <b>VT_I4</b> and subtype to <b>WIA_PROP_FLAG</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6a554b7-9e3e-4362-9dcf-fd84d9a69150">SetValidValues(FLOAT, list)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(FLOAT, list)</b> method sets the type, as well as default, current, and valid values for a <b>FLOAT</b> property associated with a list of values. The method also sets the property type to <b>VT_R4</b> and subtype to <b>WIA_PROP_LIST</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4234ce4a-5b9d-47a7-b00d-e278635ee93a">SetValidValues(FLOAT, range)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(FLOAT, range)</b> method sets the type, as well as default, current, and valid values for a <b>FLOAT</b> property associated with a range of values. The method also sets the property type to <b>VT_R4</b> and subtype to <b>WIA_PROP_RANGE</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a9a04f4-1260-4773-9c94-963fc0844ccb">SetValidValues(LONG, list)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(LONG, list)</b> method sets the type, as well as default, current, and valid values for a <b>LONG</b> property associated with a list of values. The method also sets the property type to <b>VT_I4</b> and subtype to <b>WIA_PROP_LIST</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da84a381-b564-4356-bd08-dd145b3dcc0b">SetValidValues(LONG, range)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(LONG, range)</b> method sets the type, as well as default, current, and valid values for a <b>LONG</b> property associated with a range of values. The method also sets the property type to <b>VT_I4</b> and subtype to <b>WIA_PROP_RANGE</b>.

</td>
</tr>
</table> 


## -members

The <b>CWiauPropertyList</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b847c3e-f773-44d0-a033-3e40bc2e01fc">~CWiauPropertyList</a>
</td>
<td align="left" width="63%">
The <b>~CWiauPropertyList</b> method is the destructor for the <b>CWiauPropertyList</b> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e493d3c-81b6-4db5-a550-c86eadf5a723">CWiauPropertyList</a>
</td>
<td align="left" width="63%">
The <b>CWiauPropertyList</b> method is the constructor for the <b>CWiauPropertyList</b> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/599c97af-1285-4fb9-af0b-edcd48249692">DefineProperty</a>
</td>
<td align="left" width="63%">
The <b>DefineProperty</b> method adds a property definition to a property list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a06de368-71a1-49f1-a948-1b69ca359fb6">GetPropId</a>
</td>
<td align="left" width="63%">
The <b>GetPropId</b> method finds the property ID for a property, given its index in the property list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
The <b>Init</b> method initializes a property list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/454e51fc-f81a-49c8-9e07-e32819af2642">LookupPropId</a>
</td>
<td align="left" width="63%">
The <b>LookupPropId</b> method finds a property's index, given its property ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f7d6975-4c90-4351-bf68-89786bafcc8e">SendToWia</a>
</td>
<td align="left" width="63%">
The <b>SendToWia</b> method calls the WIA service to define all of the properties currently contained in the property list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/207125d3-0833-4c5d-b66f-aa49c96a6a2d">SetAccessSubType</a>
</td>
<td align="left" width="63%">
The <b>SetAccessSubType</b> method resets a property's access and subtype.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/207125d3-0833-4c5d-b66f-aa49c96a6a2d">SetCurrentValue(BSTR)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(BSTR)</b> method sets the current value of a property of type <b>BSTR</b>, and sets its type to <b>VT_BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/017ab648-ee62-47f5-abd3-f4eac4378b8a">SetCurrentValue(BYTE*)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(BYTE*)</b> method sets the current value of a property consisting of an array of bytes, and sets its type to <b>VT_UI1</b> | <b>VT_VECTOR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0283b46-c1a2-469b-8167-f5dc63719c16">SetCurrentValue(CLSID)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(CLSID)</b> method sets the current value of a property of type <b>CLSID</b>, and sets its type to <b>VT_CLSID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfcbe65b-7da1-4427-a58f-cbec4ce355bf">SetCurrentValue(FLOAT)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(FLOAT)</b> method sets the current value of a property of type <b>FLOAT</b>, and sets its type to <b>VT_R4</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/583c8ec9-7a57-4da3-beaf-9f9db943a652">SetCurrentValue(LONG)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(LONG)</b> method sets the current value of a property of type <b>LONG</b>, and sets its type to <b>VT_I4</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1823dec6-aec8-47eb-9543-9acfd32c4b0d">SetCurrentValue(SYSTEMTIME)</a>
</td>
<td align="left" width="63%">
The <b>SetCurrentValue(SYSTEMTIME)</b> method sets the current value of a property of type <b>SYSTEMTIME</b>, and sets its type to <b>VT_UI2</b> | <b>VT_VECTOR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b806e310-4e6d-4258-8dd5-0c9aa35a35f4">SetValidValues(BSTR, list)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(BSTR, list)</b> method sets the type, as well as default, current, and valid values for a <b>BSTR</b> property associated with a list of values. The method also sets the property type to <b>VT_BSTR</b> and subtype to <b>WIA_PROP_LIST</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d401ed85-de6b-4758-b7c4-d6fcd59c157e">SetValidValues(CLSID, list)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(CLSID, list)</b> method sets the type, as well as default, current, and valid values for a <b>CLSID</b> property associated with a list of values. The method also sets the property type to <b>VT_CLSID</b> and subtype to <b>WIA_PROP_LIST</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e61b5bbb-14a8-4dfa-af36-99c5dd1ecc99">SetValidValues(flag)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(flag)</b> method sets the type, as well as default, current, and valid values for a property whose values are defined by a flag. The method also sets the property type to <b>VT_I4</b> and subtype to <b>WIA_PROP_FLAG</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6a554b7-9e3e-4362-9dcf-fd84d9a69150">SetValidValues(FLOAT, list)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(FLOAT, list)</b> method sets the type, as well as default, current, and valid values for a <b>FLOAT</b> property associated with a list of values. The method also sets the property type to <b>VT_R4</b> and subtype to <b>WIA_PROP_LIST</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4234ce4a-5b9d-47a7-b00d-e278635ee93a">SetValidValues(FLOAT, range)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(FLOAT, range)</b> method sets the type, as well as default, current, and valid values for a <b>FLOAT</b> property associated with a range of values. The method also sets the property type to <b>VT_R4</b> and subtype to <b>WIA_PROP_RANGE</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a9a04f4-1260-4773-9c94-963fc0844ccb">SetValidValues(LONG, list)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(LONG, list)</b> method sets the type, as well as default, current, and valid values for a <b>LONG</b> property associated with a list of values. The method also sets the property type to <b>VT_I4</b> and subtype to <b>WIA_PROP_LIST</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da84a381-b564-4356-bd08-dd145b3dcc0b">SetValidValues(LONG, range)</a>
</td>
<td align="left" width="63%">
The <b>SetValidValues(LONG, range)</b> method sets the type, as well as default, current, and valid values for a <b>LONG</b> property associated with a range of values. The method also sets the property type to <b>VT_I4</b> and subtype to <b>WIA_PROP_RANGE</b>.

</td>
</tr>
</table>The <b>~CWiauPropertyList</b> method is the destructor for the <b>CWiauPropertyList</b> class.

The <b>CWiauPropertyList</b> method is the constructor for the <b>CWiauPropertyList</b> class.

The <b>DefineProperty</b> method adds a property definition to a property list object.

The <b>GetPropId</b> method finds the property ID for a property, given its index in the property list.

The <b>Init</b> method initializes a property list object.

The <b>LookupPropId</b> method finds a property's index, given its property ID.

The <b>SendToWia</b> method calls the WIA service to define all of the properties currently contained in the property list object.

The <b>SetAccessSubType</b> method resets a property's access and subtype.

The <b>SetCurrentValue(BSTR)</b> method sets the current value of a property of type <b>BSTR</b>, and sets its type to <b>VT_BSTR</b>.

The <b>SetCurrentValue(BYTE*)</b> method sets the current value of a property consisting of an array of bytes, and sets its type to <b>VT_UI1</b> | <b>VT_VECTOR</b>.

The <b>SetCurrentValue(CLSID)</b> method sets the current value of a property of type <b>CLSID</b>, and sets its type to <b>VT_CLSID</b>.

The <b>SetCurrentValue(FLOAT)</b> method sets the current value of a property of type <b>FLOAT</b>, and sets its type to <b>VT_R4</b>.

The <b>SetCurrentValue(LONG)</b> method sets the current value of a property of type <b>LONG</b>, and sets its type to <b>VT_I4</b>.

The <b>SetCurrentValue(SYSTEMTIME)</b> method sets the current value of a property of type <b>SYSTEMTIME</b>, and sets its type to <b>VT_UI2</b> | <b>VT_VECTOR</b>.

The <b>SetValidValues(BSTR, list)</b> method sets the type, as well as default, current, and valid values for a <b>BSTR</b> property associated with a list of values. The method also sets the property type to <b>VT_BSTR</b> and subtype to <b>WIA_PROP_LIST</b>.

The <b>SetValidValues(CLSID, list)</b> method sets the type, as well as default, current, and valid values for a <b>CLSID</b> property associated with a list of values. The method also sets the property type to <b>VT_CLSID</b> and subtype to <b>WIA_PROP_LIST</b>.

The <b>SetValidValues(flag)</b> method sets the type, as well as default, current, and valid values for a property whose values are defined by a flag. The method also sets the property type to <b>VT_I4</b> and subtype to <b>WIA_PROP_FLAG</b>.

The <b>SetValidValues(FLOAT, list)</b> method sets the type, as well as default, current, and valid values for a <b>FLOAT</b> property associated with a list of values. The method also sets the property type to <b>VT_R4</b> and subtype to <b>WIA_PROP_LIST</b>.

The <b>SetValidValues(FLOAT, range)</b> method sets the type, as well as default, current, and valid values for a <b>FLOAT</b> property associated with a range of values. The method also sets the property type to <b>VT_R4</b> and subtype to <b>WIA_PROP_RANGE</b>.

The <b>SetValidValues(LONG, list)</b> method sets the type, as well as default, current, and valid values for a <b>LONG</b> property associated with a list of values. The method also sets the property type to <b>VT_I4</b> and subtype to <b>WIA_PROP_LIST</b>.

The <b>SetValidValues(LONG, range)</b> method sets the type, as well as default, current, and valid values for a <b>LONG</b> property associated with a range of values. The method also sets the property type to <b>VT_I4</b> and subtype to <b>WIA_PROP_RANGE</b>.

 

