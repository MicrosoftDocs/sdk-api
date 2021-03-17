---
UID: NF:propsys.IPropertySystem.GetPropertyDescriptionListFromString
title: IPropertySystem::GetPropertyDescriptionListFromString (propsys.h)
description: Gets an instance of the subsystem object that implements IPropertyDescriptionList, to obtain an ordered collection of property descriptions, based on the provided string.
helpviewer_keywords: ["GetPropertyDescriptionListFromString","GetPropertyDescriptionListFromString method [Windows Properties]","GetPropertyDescriptionListFromString method [Windows Properties]","IPropertySystem interface","IPropertySystem interface [Windows Properties]","GetPropertyDescriptionListFromString method","IPropertySystem.GetPropertyDescriptionListFromString","IPropertySystem::GetPropertyDescriptionListFromString","properties.IPropertySystem_GetPropertyDescriptionListFromString","propsys/IPropertySystem::GetPropertyDescriptionListFromString","shell.IPropertySystem_GetPropertyDescriptionListFromString","shell_IPropertySystem_GetPropertyDescriptionListFromString"]
old-location: properties\IPropertySystem_GetPropertyDescriptionListFromString.htm
tech.root: properties
ms.assetid: 73e61bf0-32d0-4c2c-bf2e-b28ea00cbfd3
ms.date: 12/05/2018
ms.keywords: GetPropertyDescriptionListFromString, GetPropertyDescriptionListFromString method [Windows Properties], GetPropertyDescriptionListFromString method [Windows Properties],IPropertySystem interface, IPropertySystem interface [Windows Properties],GetPropertyDescriptionListFromString method, IPropertySystem.GetPropertyDescriptionListFromString, IPropertySystem::GetPropertyDescriptionListFromString, properties.IPropertySystem_GetPropertyDescriptionListFromString, propsys/IPropertySystem::GetPropertyDescriptionListFromString, shell.IPropertySystem_GetPropertyDescriptionListFromString, shell_IPropertySystem_GetPropertyDescriptionListFromString
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Propsys.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IPropertySystem::GetPropertyDescriptionListFromString
 - propsys/IPropertySystem::GetPropertyDescriptionListFromString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.dll
api_name:
 - IPropertySystem.GetPropertyDescriptionListFromString
---

# IPropertySystem::GetPropertyDescriptionListFromString


## -description

Gets an instance of the subsystem object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a>, to obtain an ordered collection of property descriptions, based on the provided string.

## -parameters

### -param pszPropList [in]

Type: <b>LPCWSTR</b>

A pointer to a string that identifies the property list.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired IID.

### -param ppv [out]

Type: <b>void**</b>

The address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Indicates interface is obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates <i>ppv</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The property description list string ("proplist") syntax consists of a sequence of canonical property names, with flags associated with each property name. The string starts with "prop:". The syntax looks like this: <code>prop:[flags]propertyname[endflags];</code>

The flags are optional and can be any of those below. Note: These flags translate to the <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_view_flags">PROPDESC_VIEW_FLAGS</a> enum.

<table class="clsStd">
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>-</td>
<td>Sort in reverse order (PDVF_REVERSESORT).</td>
</tr>
<tr>
<td>0</td>
<td>Show by default in both the primary and secondary lists (PDVF_SHOWBYDEFAULT | PDVF_SHOWINPRIMARYLIST | PDVF_SHOWINSECONDARYLIST).</td>
</tr>
<tr>
<td>1</td>
<td>Show in the primary and secondary lists (PDVF_SHOWINPRIMARYLIST | PDVF_SHOWINSECONDARYLIST).</td>
</tr>
<tr>
<td>2</td>
<td>Show in secondary list (PDVF_SHOWINSECONDARYLIST).</td>
</tr>
<tr>
<td>^</td>
<td>Begin a new group (PDVF_BEGINNEWGROUP).</td>
</tr>
<tr>
<td>/</td>
<td>Right align (PDVF_RIGHTALIGN).</td>
</tr>
<tr>
<td>*</td>
<td>Hide if the value is not present.</td>
</tr>
<tr>
<td>|</td>
<td>Center align. (PDVF_CENTERALIGN).</td>
</tr>
<tr>
<td>~</td>
<td>Hide the label. (PDVF_HIDELABEL).</td>
</tr>
<tr>
<td>#</td>
<td>Fill area. (PDVF_FILLAREA).</td>
</tr>
<tr>
<td>?</td>
<td>Hide if unsupported by property handler (PDVF_HIDEIFUNSUPPORTED).</td>
</tr>
<tr>
<td>&lt;</td>
<td>Parse as link (PDVF_PARSEASLINK).</td>
</tr>
<tr>
<td>&amp;</td>
<td>Show as whole link (PDVF_SHOWASWHOLELINK).</td>
</tr>
</table>
 

From the dbfolder and file folder perspective:

<table class="clsStd">
<tr>
<td>0</td>
<td>Show as a column in defview, column chooser menu, and column chooser dialog.</td>
</tr>
<tr>
<td>1</td>
<td>Show in the column chooser menu and dialog.</td>
</tr>
<tr>
<td>2</td>
<td>Show in the column chooser dialog.</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td>Include in the search results, but hide in the UI.</td>
</tr>
</table>
 

The endflags are also optional and can be the following:

<table class="clsStd">
<tr>
<th>EndFlag</th>
<th>Meaning</th>
</tr>
<tr>
<td>]</td>
<td>End column (used for extended tiles view).</td>
</tr>
</table>
 

It is recommended that you use the IID_PPV_ARGS macro, defined in objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, eliminating the possibility of a coding error.

For more information about property schemas, see 
            <a href="/windows/desktop/properties/building-property-handlers-property-schemas">Property Schemas</a>.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a>