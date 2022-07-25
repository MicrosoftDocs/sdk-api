---
UID: NF:gdipluseffects.Effect.GetAuxData
title: Effect::GetAuxData (gdipluseffects.h)
description: The Effect::GetAuxData gets a pointer to a set of lookup tables created by a previous call to the Bitmap::ApplyEffect method.
helpviewer_keywords: ["Effect class [GDI+]","GetAuxData method","Effect.GetAuxData","Effect::GetAuxData","GetAuxData","GetAuxData method [GDI+]","GetAuxData method [GDI+]","Effect class","_gdiplus_CLASS_Effect_GetAuxData_","gdiplus._gdiplus_CLASS_Effect_GetAuxData_"]
old-location: gdiplus\_gdiplus_CLASS_Effect_GetAuxData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effectclass\effectmethods\getauxdata.htm
ms.date: 12/05/2018
ms.keywords: Effect class [GDI+],GetAuxData method, Effect.GetAuxData, Effect::GetAuxData, GetAuxData, GetAuxData method [GDI+], GetAuxData method [GDI+],Effect class, _gdiplus_CLASS_Effect_GetAuxData_, gdiplus._gdiplus_CLASS_Effect_GetAuxData_
req.header: gdipluseffects.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Effect::GetAuxData
 - gdipluseffects/Effect::GetAuxData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Effect.GetAuxData
---

# Effect::GetAuxData


## -description

The <b>Effect::GetAuxData</b> gets a pointer to a set of lookup tables created by a previous call to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.



## -returns

This method returns a pointer to a set of lookup tables created by a previous call to <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a>. If no lookup tables are available, the return value is <b>NULL</b>.

## -remarks

You can apply an effect to a bitmap by creating an instance of one of the descendants of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a> class and passing the address of that descendant to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. For certain descendants of <b>Effect</b>, ApplyEffect creates lookup tables and returns the address of those tables to the descendant object. For example, you can retrieve the lookup tables for a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object as follows:

<ol>
<li>Create a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object and call its <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-brightnesscontrast-setparameters">SetParameters</a> method.</li>
<li>Pass <b>TRUE</b> to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-useauxdata">Effect::UseAuxData</a> method of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
<li>Call the <b>Effect::GetAuxData</b> method of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object to obtain a pointer to the lookup tables created by <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">ApplyEffect</a>. The buffer for the lookup tables is allocated by ApplyEffect; you are not responsible for freeing the buffer.</li>
</ol>

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">ApplyEffect</a> can return the address of lookup tables for the following descendants of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a> class.

<ul>
<li>
<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-huesaturationlightness">HueSaturationLightness</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-levels">Levels</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorbalance">ColorBalance</a>
</li>
<li>
<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorcurve">ColorCurve</a>
</li>
</ul>
For the classes in the preceding list, <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">ApplyEffect</a> creates four lookup tables: one each for the blue, green, red, and alpha channels. Each lookup table is an array of 256 bytes so the size of the entire set of tables is 1024 bytes. The tables are stored in the order blue, green, red, alpha.


#### Examples



The following code passes the address of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. Then the code prints the blue-channel lookup table created by ApplyEffect.


```cpp
Bitmap bm(L"Picture.bmp");

BrightnessContrastParams briConParams;
briConParams.brightnessLevel = 0;
briConParams.contrastLevel = 25;

BrightnessContrast briCon;
briCon.SetParameters(&briConParams);
briCon.UseAuxData(TRUE);
	
bm.ApplyEffect(&briCon, NULL);

VOID* data = briCon.GetAuxData();

// You know the size is 1024, but check to make sure.
INT size = briCon.GetAuxDataSize();

if(1024 != size || NULL == data)
   return;

// Cast the data pointer as a ColorLUTParams pointer so that it
// will be easy to examine the individual tables.
ColorLUTParams* tables = (ColorLUTParams*)data;
   
// Print the lookup table for the blue channel.
for(UINT j = 0; j < 256; ++j)
{
   printf("%u, %u\n", j, tables->lutB[j]);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorlutparams">ColorLUTParams</a>



<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-getauxdatasize">Effect::GetAuxDataSize</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-useauxdata">Effect::UseAuxData</a>
