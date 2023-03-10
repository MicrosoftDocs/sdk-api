---
UID: NF:vbinterf.IVBGetControl.EnumControls
title: IVBGetControl::EnumControls (vbinterf.h)
description: Enumerates the controls on the form.
helpviewer_keywords: ["EnumControls","EnumControls method [COM]","EnumControls method [COM]","IVBGetControl interface","GCW_WCH_SIBLING","GC_WCH_ALL","GC_WCH_CONTAINED","GC_WCH_CONTAINER","GC_WCH_FONLYAFTER","GC_WCH_FONLYBEFORE","GC_WCH_FREVERSEDIR","GC_WCH_FSELECTED","IVBGetControl interface [COM]","EnumControls method","IVBGetControl.EnumControls","IVBGetControl::EnumControls","OLECONTF_EMBEDDINGS","OLECONTF_LINKS","OLECONTF_ONLYIFRUNNING","OLECONTF_ONLYUSER","OLECONTF_OTHER","_com_IVBGetControl_EnumControls","com.ivbgetcontrol_enumcontrols","vbinterf/IVBGetControl::EnumControls"]
old-location: com\ivbgetcontrol_enumcontrols.htm
tech.root: com
ms.assetid: 4ae01518-8762-4bce-ad9c-4dc2635e743d
ms.date: 12/05/2018
ms.keywords: EnumControls, EnumControls method [COM], EnumControls method [COM],IVBGetControl interface, GCW_WCH_SIBLING, GC_WCH_ALL, GC_WCH_CONTAINED, GC_WCH_CONTAINER, GC_WCH_FONLYAFTER, GC_WCH_FONLYBEFORE, GC_WCH_FREVERSEDIR, GC_WCH_FSELECTED, IVBGetControl interface [COM],EnumControls method, IVBGetControl.EnumControls, IVBGetControl::EnumControls, OLECONTF_EMBEDDINGS, OLECONTF_LINKS, OLECONTF_ONLYIFRUNNING, OLECONTF_ONLYUSER, OLECONTF_OTHER, _com_IVBGetControl_EnumControls, com.ivbgetcontrol_enumcontrols, vbinterf/IVBGetControl::EnumControls
req.header: vbinterf.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVBGetControl::EnumControls
 - vbinterf/IVBGetControl::EnumControls
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VbInterf.h
api_name:
 - IVBGetControl.EnumControls
---

# IVBGetControl::EnumControls


## -description

Enumerates the controls on the form.
<div class="alert"><b>Note</b>  The use of this method is no longer recommended because containers other than Visual Basic do not support 
    it.</div><div> </div>

## -parameters

### -param dwOleContF [in]

Specifies the type of OLE objects to be enumerated. This parameter can be one of the following 
      values enumerated by the <a href="/windows/desktop/api/oleidl/ne-oleidl-olecontf">OLECONTF</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OLECONTF_EMBEDDINGS"></a><a id="olecontf_embeddings"></a><dl>
<dt><b>OLECONTF_EMBEDDINGS</b></dt>
</dl>
</td>
<td width="60%">
Enumerates the embedded objects on the form. Include this flag to enumerate OLE controls.

</td>
</tr>
<tr>
<td width="40%"><a id="OLECONTF_LINKS"></a><a id="olecontf_links"></a><dl>
<dt><b>OLECONTF_LINKS</b></dt>
</dl>
</td>
<td width="60%">
Enumerates the linked objects on the form.

</td>
</tr>
<tr>
<td width="40%"><a id="OLECONTF_OTHER"></a><a id="olecontf_other"></a><dl>
<dt><b>OLECONTF_OTHER</b></dt>
</dl>
</td>
<td width="60%">
Enumerates all pseudo OLE objects. Include this flag to enumerate VBX controls.

</td>
</tr>
<tr>
<td width="40%"><a id="OLECONTF_ONLYUSER"></a><a id="olecontf_onlyuser"></a><dl>
<dt><b>OLECONTF_ONLYUSER</b></dt>
</dl>
</td>
<td width="60%">
Enumerates only objects that the user is aware of.

</td>
</tr>
<tr>
<td width="40%"><a id="OLECONTF_ONLYIFRUNNING"></a><a id="olecontf_onlyifrunning"></a><dl>
<dt><b>OLECONTF_ONLYIFRUNNING</b></dt>
</dl>
</td>
<td width="60%">
Enumerates only the objects that are running on the form.

</td>
</tr>
</table>
 

When enumerating OLE controls, it is recommended that you combine the flags 
      <b>OLECONTF_ONLYUSER</b>, <b>OLECONTF_ONLYIFRUNNING</b>, and 
      <b>OLECONTF_EMBEDDINGS</b>. To include both OLE controls and VBX controls, add the 
      <b>OLECONTF_OTHERS</b> flag to this list. To enumerate only VBX controls, remove the 
      <b>OLECONTF_EMBEDDINGS</b> flag and include the <b>OLECONTF_OTHERS</b> 
      flag.

### -param dwWhich [in]

Specifies the set of controls to be enumerated. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCW_WCH_SIBLING"></a><a id="gcw_wch_sibling"></a><dl>
<dt><b>GCW_WCH_SIBLING</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enumerates all siblings of the control.

</td>
</tr>
<tr>
<td width="40%"><a id="GC_WCH_CONTAINER"></a><a id="gc_wch_container"></a><dl>
<dt><b>GC_WCH_CONTAINER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Enumerates all objects that are parents of your control. You cannot use the 
        <b>GC_WCH_FONLYAFTER</b> or <b>GC_WCH_FONLYBEFORE</b> flags with this 
        flag.

</td>
</tr>
<tr>
<td width="40%"><a id="GC_WCH_CONTAINED"></a><a id="gc_wch_contained"></a><dl>
<dt><b>GC_WCH_CONTAINED</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Enumerates all objects that are children of your control. You cannot use the 
        <b>GC_WCH_FONLYAFTER</b> or <b>GC_WCH_FONLYBEFORE</b> flags with this 
        flag.

</td>
</tr>
<tr>
<td width="40%"><a id="GC_WCH_ALL"></a><a id="gc_wch_all"></a><dl>
<dt><b>GC_WCH_ALL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Enumerates all objects.

</td>
</tr>
<tr>
<td width="40%"><a id="GC_WCH_FREVERSEDIR"></a><a id="gc_wch_freversedir"></a><dl>
<dt><b>GC_WCH_FREVERSEDIR</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
Enumerates and organizes controls in the reverse tab order direction. This flag can be combined with any 
        other flag.

</td>
</tr>
<tr>
<td width="40%"><a id="GC_WCH_FONLYAFTER"></a><a id="gc_wch_fonlyafter"></a><dl>
<dt><b>GC_WCH_FONLYAFTER</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Enumerates all controls that appear after your control in the tab order.

</td>
</tr>
<tr>
<td width="40%"><a id="GC_WCH_FONLYBEFORE"></a><a id="gc_wch_fonlybefore"></a><dl>
<dt><b>GC_WCH_FONLYBEFORE</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Enumerates all controls that appear before your control in the tab order.

</td>
</tr>
<tr>
<td width="40%"><a id="GC_WCH_FSELECTED"></a><a id="gc_wch_fselected"></a><dl>
<dt><b>GC_WCH_FSELECTED</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Enumerates all the controls that are currently selected.

</td>
</tr>
</table>
 

Use one of the flags <b>GC_WCH_SIBLING</b>, <b>GC_WCH_CONTAINER</b>, 
       <b>GC_WCH_CONTAINED</b>, or <b>GC_WCH_ALL</b> in combination with any of 
       the GC_WCH_F<i>xxx</i> flags.

In VBX code, the GC_FORM flag was passed to <b>VBGetControl</b> to obtain a pointer to 
       the form. In OLE control code, there is no direct replacement for this flag. Instead, pass 
       <b>GC_WHC_ALL</b> to 
       <b>EnumControls</b> and use the pointer to the 
       first control in the enumeration. The first control in the enumeration is always the form when using 
       <b>GC_WHC_ALL</b>.

### -param ppenumUnk [out]

Pointer to an enumeration of OLE objects.

## -returns

This method supports the standard return values <b>E_INVALIDARG</b>, 
      <b>E_OUTOFMEMORY</b>, and <b>E_UNEXPECTED</b>, as well as the 
      following:

## -remarks

When migrating a VBX control to an OLE control, 
    <b>EnumControls</b> replaces the Visual Basic 
    <b>VBGetControl</b>, which is no longer supported.

## -see-also

<a href="/windows/desktop/api/vbinterf/nn-vbinterf-ivbgetcontrol">IVBGetControl</a>



<a href="/windows/desktop/api/oleidl/ne-oleidl-olecontf">OLECONTF</a>