---
UID: NF:gdiplusheaders.Metafile.GetHENHMETAFILE
title: Metafile::GetHENHMETAFILE
author: windows-sdk-content
description: The Metafile::GetHENHMETAFILE method gets a Windows handle to an Enhanced Metafile (EMF) file.
old-location: gdiplus\_gdiplus_CLASS_Metafile_GetHENHMETAFILE_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafilemethods\gethenhmetafile.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetHENHMETAFILE, GetHENHMETAFILE method [GDI+], GetHENHMETAFILE method [GDI+],Metafile class, Metafile class [GDI+],GetHENHMETAFILE method, Metafile.GetHENHMETAFILE, Metafile::GetHENHMETAFILE, _gdiplus_CLASS_Metafile_GetHENHMETAFILE_, gdiplus._gdiplus_CLASS_Metafile_GetHENHMETAFILE_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Metafile.GetHENHMETAFILE
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Metafile::GetHENHMETAFILE


## -description


The <b>Metafile::GetHENHMETAFILE</b> method gets a Windows handle to an Enhanced Metafile (EMF) file.


## -parameters






## -returns



Type: <strong>Type: <b>HENHMETAFILE</b>
</strong>

This method returns a 

						<b>HENHMETAFILE</b>.




## -remarks



This method sets the 

				<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> object to an invalid state. The user is responsible for calling DeleteEnhMetafile, to delete the Windows handle.


#### Examples



The following example creates a 

						<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> object from an EMF+ file and gets a Windows handle to the metafile.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetHENHMETAFILE(HDC hdc)
{

   // Create a GDI+ Metafile object from an existing disk file.
   Metafile metafile(L"SampleMetafile.emf+");

   // Get a Windows handle to the metafile.
   HENHMETAFILE hEmf = metafile.GetHENHMETAFILE();

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/48cacd83-8123-476c-af78-11ad41285c3e">ENHMETAHEADER3</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>
 

 

