---
UID: NF:mmc.IExtendPropertySheet2.GetWatermarks
title: IExtendPropertySheet2::GetWatermarks (mmc.h)
description: The IExtendPropertySheet2::GetWatermarks method gets the watermark bitmap and header bitmap for wizard sheets implemented as Wizard 97-style wizards.
helpviewer_keywords: ["GetWatermarks","GetWatermarks method [MMC]","GetWatermarks method [MMC]","IExtendPropertySheet2 interface","IExtendPropertySheet2 interface [MMC]","GetWatermarks method","IExtendPropertySheet2.GetWatermarks","IExtendPropertySheet2::GetWatermarks","_slate_iextendpropertysheet2_getwatermarks","mmc.iextendpropertysheet2_getwatermarks","mmc/IExtendPropertySheet2::GetWatermarks"]
old-location: mmc\iextendpropertysheet2_getwatermarks.htm
tech.root: mmc
ms.assetid: caecb35a-3f59-4a04-af46-862ded9685cf
ms.date: 12/05/2018
ms.keywords: GetWatermarks, GetWatermarks method [MMC], GetWatermarks method [MMC],IExtendPropertySheet2 interface, IExtendPropertySheet2 interface [MMC],GetWatermarks method, IExtendPropertySheet2.GetWatermarks, IExtendPropertySheet2::GetWatermarks, _slate_iextendpropertysheet2_getwatermarks, mmc.iextendpropertysheet2_getwatermarks, mmc/IExtendPropertySheet2::GetWatermarks
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - IExtendPropertySheet2::GetWatermarks
 - mmc/IExtendPropertySheet2::GetWatermarks
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendPropertySheet2.GetWatermarks
---

# IExtendPropertySheet2::GetWatermarks


## -description

The <b>IExtendPropertySheet2::GetWatermarks</b> method gets the watermark bitmap and header bitmap for wizard sheets implemented as Wizard 97-style wizards.

## -parameters

### -param lpIDataObject [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the object that contains context information about the scope or result item.

### -param lphWatermark [out]

A pointer to the handle to a bitmap that serves as the watermark for Wizard 97 pages. If the handle to the bitmap is <b>NULL</b>, no watermark is displayed for the wizard. If this value is not <b>NULL</b>, then the snap-in, for compatibility, should manage the lifetime of the watermark resource. The snap-in is responsible for freeing the watermark resource.

### -param lphHeader [out]

A pointer to the handle to a bitmap that serves as the header for Wizard 97 pages. If the handle to the bitmap is <b>NULL</b>, no bitmap will be displayed in the header for wizard pages. If this value is not <b>NULL</b>, then the snap-in, for compatibility, should manage the lifetime of the header resource. The snap-in is responsible for freeing the header resource.

### -param lphPalette [out]

A pointer to the handle to a palette that should be used for the bitmaps specified by lphWatermark and lphHeader. The palette is <b>NULL</b> by default. If a palette is not returned, the palette is <b>NULL</b>. If this value is not <b>NULL</b>, then the snap-in, for compatibility, should manage the lifetime of the palette resource. The snap-in is responsible for freeing the palette resource.

### -param bStretch [out]

A value that specifies whether the watermark and header bitmaps should be stretched — instead of tiled — to fit the background or header area of the property sheet. <b>TRUE</b> specifies that the watermark and header bitmaps should be stretched; <b>FALSE</b> specifies that the watermark and header bitmaps should maintain their size and be tiled. This parameter is <b>FALSE</b> by default. If a <i>bStretch</i> value is not returned, <i>bStretch</i> is <b>FALSE</b>.

## -returns

This method can return one of these values.

## -remarks

MMC calls this method only when:

<ol>
<li>The type parameter of 
<a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-createpropertysheet">IPropertySheetProvider::CreatePropertySheet</a> is set to <b>FALSE</b> (for wizard sheet) and that the <i>dwOptions</i> parameter is set to <b>MMC_PSO_NEWWIZARDTYPE</b> (for Wizard 97 style).</li>
<li>The snap-in passes a pointer to its 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> or 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> interface as the first parameter in calls to the 
<a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-addprimarypages">IPropertySheetProvider::AddPrimaryPages</a> method.</li>
</ol>
If the snap-in's implementation of this method returns a failure value (such as <b>E_NOTIMPL</b>), MMC reverts the wizard sheet requested by the snap-in in the call to <a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-createpropertysheet">IPropertySheetProvider::CreatePropertySheet</a> to the non-Wizard 97 style. This is to maintain compatibility with MMC 1.1.

To prevent distortion of the image, it is recommended that the watermark and header bitmaps have the following dimensions (in pixels) with <i>bStretch</i> set to <b>FALSE</b>.

<table>
<tr>
<th>Bitmap</th>
<th>Dimensions</th>
</tr>
<tr>
<td><i>lphWatermark</i></td>
<td>164w x 628h</td>
</tr>
<tr>
<td><i>lphHeader</i></td>
<td>49w x 49h</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mmc/adding-property-pages-and-wizard-pages">Adding Property Pages and Wizard Pages</a>



<a href="/previous-versions/windows/desktop/mmc/adding-wizard-pages-implementation-details">Adding Wizard Pages: Implementation Details</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendpropertysheet2">IExtendPropertySheet2</a>