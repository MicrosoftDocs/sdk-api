---
UID: NF:gdipluseffects.Effect.GetAuxData
title: Effect::GetAuxData
author: windows-sdk-content
description: The Effect::GetAuxData gets a pointer to a set of lookup tables created by a previous call to the Bitmap::ApplyEffect method.
old-location: gdiplus\_gdiplus_CLASS_Effect_GetAuxData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effectclass\effectmethods\getauxdata.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Effect class [GDI+],GetAuxData method, Effect.GetAuxData, Effect::GetAuxData, GetAuxData, GetAuxData method [GDI+], GetAuxData method [GDI+],Effect class, _gdiplus_CLASS_Effect_GetAuxData_, gdiplus._gdiplus_CLASS_Effect_GetAuxData_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Effect.GetAuxData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Effect::GetAuxData


## -description


The <b>Effect::GetAuxData</b> gets a pointer to a set of lookup tables created by a previous call to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.


## -parameters






## -returns



This method returns a pointer to a set of lookup tables created by a previous call to <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a>. If no lookup tables are available, the return value is <b>NULL</b>.




## -remarks



You can apply an effect to a bitmap by creating an instance of one of the descendants of the <a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a> class and passing the address of that descendant to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. For certain descendants of <b>Effect</b>, ApplyEffect creates lookup tables and returns the address of those tables to the descendant object. For example, you can retrieve the lookup tables for a <a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a> object as follows:

<ol>
<li>Create a <a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a> object and call its <a href="https://msdn.microsoft.com/ca9e5978-75ff-4e06-9597-0e706db19259">SetParameters</a> method.</li>
<li>Pass <b>TRUE</b> to the <a href="https://msdn.microsoft.com/b9644e8d-a5d3-47ac-bd6a-6c720ef714f5">Effect::UseAuxData</a> method of the <a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a> object to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
<li>Call the <b>Effect::GetAuxData</b> method of the <a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a> object to obtain a pointer to the lookup tables created by <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">ApplyEffect</a>. The buffer for the lookup tables is allocated by ApplyEffect; you are not responsible for freeing the buffer.</li>
</ol>

<a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">ApplyEffect</a> can return the address of lookup tables for the following descendants of the <a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a> class.

<ul>
<li>
<a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3bb652eb-62f0-4948-9484-4439dc9bd54e">HueSaturationLightness</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0256fa03-f029-472e-988a-9eb7ed117673">Levels</a>
</li>
<li>
<a href="https://msdn.microsoft.com/87366bae-a67a-46bd-b06c-2c80b80ab800">ColorBalance</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a>
</li>
</ul>
For the classes in the preceding list, <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">ApplyEffect</a> creates four lookup tables: one each for the blue, green, red, and alpha channels. Each lookup table is an array of 256 bytes so the size of the entire set of tables is 1024 bytes. The tables are stored in the order blue, green, red, alpha.


#### Examples



The following code passes the address of a <a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a> object to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. Then the code prints the blue-channel lookup table created by ApplyEffect.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Bitmap bm(L"Picture.bmp");

BrightnessContrastParams briConParams;
briConParams.brightnessLevel = 0;
briConParams.contrastLevel = 25;

BrightnessContrast briCon;
briCon.SetParameters(&amp;briConParams);
briCon.UseAuxData(TRUE);
	
bm.ApplyEffect(&amp;briCon, NULL);

VOID* data = briCon.GetAuxData();

// You know the size is 1024, but check to make sure.
INT size = briCon.GetAuxDataSize();

if(1024 != size || NULL == data)
   return;

// Cast the data pointer as a ColorLUTParams pointer so that it
// will be easy to examine the individual tables.
ColorLUTParams* tables = (ColorLUTParams*)data;
   
// Print the lookup table for the blue channel.
for(UINT j = 0; j &lt; 256; ++j)
{
   printf("%u, %u\n", j, tables-&gt;lutB[j]);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6ae866ac-6335-428a-bb11-ec793b69c2b7">ColorLUTParams</a>



<a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a>



<a href="https://msdn.microsoft.com/c19c3891-2894-4655-b5c8-1306bfb72244">Effect::GetAuxDataSize</a>



<a href="https://msdn.microsoft.com/b9644e8d-a5d3-47ac-bd6a-6c720ef714f5">Effect::UseAuxData</a>
 

 

