---
UID: NF:mmc.IExtendPropertySheet2.GetWatermarks
title: IExtendPropertySheet2::GetWatermarks
author: windows-sdk-content
description: The IExtendPropertySheet2::GetWatermarks method gets the watermark bitmap and header bitmap for wizard sheets implemented as Wizard 97-style wizards.
old-location: mmc\iextendpropertysheet2_getwatermarks.htm
old-project: mmc
ms.assetid: caecb35a-3f59-4a04-af46-862ded9685cf
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetWatermarks, GetWatermarks method [MMC], GetWatermarks method [MMC],IExtendPropertySheet2 interface, IExtendPropertySheet2 interface [MMC],GetWatermarks method, IExtendPropertySheet2.GetWatermarks, IExtendPropertySheet2::GetWatermarks, _slate_iextendpropertysheet2_getwatermarks, mmc.iextendpropertysheet2_getwatermarks, mmc/IExtendPropertySheet2::GetWatermarks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendPropertySheet2.GetWatermarks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IExtendPropertySheet2::GetWatermarks


## -description


The <b>IExtendPropertySheet2::GetWatermarks</b> method gets the watermark bitmap and header bitmap for wizard sheets implemented as Wizard 97-style wizards.


## -parameters




### -param lpIDataObject [in]

A pointer to the 
<a href="_ole_idataobject">IDataObject</a> interface on the object that contains context information about the scope or result item.


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
<a href="https://msdn.microsoft.com/8d53083a-d578-4a88-bd3f-d43c88d697e5">IPropertySheetProvider::CreatePropertySheet</a> is set to <b>FALSE</b> (for wizard sheet) and that the <i>dwOptions</i> parameter is set to <b>MMC_PSO_NEWWIZARDTYPE</b> (for Wizard 97 style).</li>
<li>The snap-in passes a pointer to its 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> or 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> interface as the first parameter in calls to the 
<a href="https://msdn.microsoft.com/f555dfd0-8af3-422f-a339-ab79daa89b45">IPropertySheetProvider::AddPrimaryPages</a> method.</li>
</ol>
If the snap-in's implementation of this method returns a failure value (such as <b>E_NOTIMPL</b>), MMC reverts the wizard sheet requested by the snap-in in the call to <a href="https://msdn.microsoft.com/8d53083a-d578-4a88-bd3f-d43c88d697e5">IPropertySheetProvider::CreatePropertySheet</a> to the non-Wizard 97 style. This is to maintain compatibility with MMC 1.1.

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




<a href="https://msdn.microsoft.com/b41508bf-8399-44bb-abad-754aa5d32776">Adding Property Pages and Wizard Pages</a>



<a href="https://msdn.microsoft.com/d00e0e6d-3416-47c0-8d70-dcdacba220d0">Adding Wizard Pages: Implementation Details</a>



<a href="https://msdn.microsoft.com/9beb0a0a-b3bf-46d0-b10c-0fc3ab25c18d">IExtendPropertySheet2</a>
 

 

