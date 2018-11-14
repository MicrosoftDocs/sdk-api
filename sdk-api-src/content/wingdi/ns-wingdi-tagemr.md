---
UID: NS:wingdi.tagEMR
title: tagEMR
author: windows-sdk-content
description: The EMR structure provides the base structure for all enhanced metafile records. An enhanced metafile record contains the parameters for a specific GDI function used to create part of a picture in an enhanced format metafile.
old-location: gdi\emr.htm
tech.root: gdi
ms.assetid: 06582047-b64b-44ec-ae27-1f8ed7c56b97
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PEMR, EMR, EMR structure [Windows GDI], PEMR, PEMR structure pointer [Windows GDI], _win32_EMR_str, gdi.emr, tagEMR, wingdi/EMR, wingdi/PEMR"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMR
product: Windows
targetos: Windows
req.typenames: EMR, *PEMR
req.redist: 
---

# tagEMR structure


## -description



The <b>EMR</b> structure provides the base structure for all enhanced metafile records. An enhanced metafile record contains the parameters for a specific GDI function used to create part of a picture in an enhanced format metafile.




## -struct-fields




### -field iType

The record type. The parameter can be one of the following (with a link to the associated record structure).

<a href="https://msdn.microsoft.com/ee9f57af-8d96-4b85-b8ab-4eb57e6c7c78">EMR_ABORTPATH</a>
<a href="https://msdn.microsoft.com/3270d8ed-a174-4d77-a9a7-3e3f0cab2a23">EMR_ALPHABLEND</a>
<a href="https://msdn.microsoft.com/054b84ba-bb5e-4dca-8482-6b958151aedf">EMR_ANGLEARC</a>
<a href="https://msdn.microsoft.com/f249b396-bf71-401b-b972-317d551fc9aa">EMR_ARC</a>
<a href="https://msdn.microsoft.com/f249b396-bf71-401b-b972-317d551fc9aa">EMR_ARCTO</a>
<a href="https://msdn.microsoft.com/ee9f57af-8d96-4b85-b8ab-4eb57e6c7c78">EMR_BEGINPATH</a>
<a href="https://msdn.microsoft.com/ed3dbed6-4a2c-4fba-a803-f407fe60d750">EMR_BITBLT</a>
<a href="https://msdn.microsoft.com/f249b396-bf71-401b-b972-317d551fc9aa">EMR_CHORD</a>
<a href="https://msdn.microsoft.com/ee9f57af-8d96-4b85-b8ab-4eb57e6c7c78">EMR_CLOSEFIGURE</a>
<a href="https://msdn.microsoft.com/12e31e22-b9ac-454d-a423-b3fee582fcba">EMR_COLORCORRECTPALETTE</a>
<a href="https://msdn.microsoft.com/9b89b703-b670-40eb-b95f-d07e8731e71b">EMR_COLORMATCHTOTARGETW</a>
<a href="https://msdn.microsoft.com/fd87d52a-1227-48ba-8b7e-a8fd007c9d01">EMR_CREATEBRUSHINDIRECT</a>
<a href="https://msdn.microsoft.com/ee2e02bb-5bd2-460c-aefe-78a143c72ff6">EMR_CREATECOLORSPACE</a>
<a href="https://msdn.microsoft.com/eac364ad-ef17-4f60-ac4c-39d8a9af618b">EMR_CREATECOLORSPACEW</a>
<a href="https://msdn.microsoft.com/e1d8302b-9dbe-4a92-9143-7ad03e334ee5">EMR_CREATEDIBPATTERNBRUSHPT</a>
<a href="https://msdn.microsoft.com/6f581ad4-0449-40b1-bcc6-737bfcdc33c4">EMR_CREATEMONOBRUSH</a>
<a href="https://msdn.microsoft.com/5198dc94-49bf-4cc8-8b41-2f29acd3c17d">EMR_CREATEPALETTE</a>
<a href="https://msdn.microsoft.com/bd338c56-00b4-4eae-9e4f-57ac49809f32">EMR_CREATEPEN</a>
<a href="https://msdn.microsoft.com/c661b3cc-6b41-4157-acb4-f9083ab73851">EMR_DELETECOLORSPACE</a>
<a href="https://msdn.microsoft.com/02ec5839-3390-429b-8f0c-6f2e74393c8f">EMR_DELETEOBJECT</a>
<a href="https://msdn.microsoft.com/1400f9d7-4ccd-4348-98f0-fccc78e06212">EMR_ELLIPSE</a>
<a href="https://msdn.microsoft.com/ee9f57af-8d96-4b85-b8ab-4eb57e6c7c78">EMR_ENDPATH</a>
<a href="https://msdn.microsoft.com/99a3f97e-cb43-49b3-9972-23f9911b2cd0">EMR_EOF</a>
<a href="https://msdn.microsoft.com/a8969bfd-cd60-485f-bbcc-4bf015526d56">EMR_EXCLUDECLIPRECT</a>
<a href="https://msdn.microsoft.com/27adba1d-6845-4d5e-8183-9c092775b473">EMR_EXTCREATEFONTINDIRECTW</a>
<a href="https://msdn.microsoft.com/9ed97d34-8c03-4b14-821c-397c21c36db0">EMR_EXTCREATEPEN</a>
<a href="https://msdn.microsoft.com/93c80ea4-42f3-4c0a-8f72-76d2a6634e15">EMR_EXTFLOODFILL</a>
<a href="https://msdn.microsoft.com/fcfa0ae1-06e0-4313-9140-496aa4eec9da">EMR_EXTSELECTCLIPRGN</a>
<a href="https://msdn.microsoft.com/1d9b0b32-6a51-481a-9589-3de832d746d7">EMR_EXTTEXTOUTA</a>
<a href="https://msdn.microsoft.com/1d9b0b32-6a51-481a-9589-3de832d746d7">EMR_EXTTEXTOUTW</a>
<a href="https://msdn.microsoft.com/9911e0fb-2e0d-4684-bff6-fc876ab8185d">EMR_FILLPATH</a>
<a href="https://msdn.microsoft.com/84b81b9d-3def-403c-94cd-8f5ddea02d6d">EMR_FILLRGN</a>
<a href="https://msdn.microsoft.com/ee9f57af-8d96-4b85-b8ab-4eb57e6c7c78">EMR_FLATTENPATH</a>
<a href="https://msdn.microsoft.com/578a2824-b42e-401d-b4b0-8426440713c6">EMR_FRAMERGN</a>
<a href="https://msdn.microsoft.com/aac18154-bd50-45a4-a1ba-390b59525fa9">EMR_GDICOMMENT</a>
<a href="https://msdn.microsoft.com/0e397451-543c-4278-9cdd-fbd276b646dd">EMR_GLSBOUNDEDRECORD</a>
<a href="https://msdn.microsoft.com/58e31199-80e2-4077-a6f6-1787c5228f77">EMR_GLSRECORD</a>
<a href="https://msdn.microsoft.com/efd12e71-ee26-4fc8-8e9f-5b0105ebe057">EMR_GRADIENTFILL</a>
<a href="https://msdn.microsoft.com/a8969bfd-cd60-485f-bbcc-4bf015526d56">EMR_INTERSECTCLIPRECT</a>
<a href="https://msdn.microsoft.com/91c0badc-bd26-418a-9cdb-3e70e7337021">EMR_INVERTRGN</a>
<a href="https://msdn.microsoft.com/876db90d-3775-48e8-8911-e6612a3484ae">EMR_LINETO</a>
<a href="https://msdn.microsoft.com/4c9e8631-8b76-423f-9691-8c93c6412d41">EMR_MASKBLT</a>
<a href="https://msdn.microsoft.com/61d51fc9-a8dd-4981-940d-eedc8936360a">EMR_MODIFYWORLDTRANSFORM</a>
<a href="https://msdn.microsoft.com/876db90d-3775-48e8-8911-e6612a3484ae">EMR_MOVETOEX</a>
<a href="https://msdn.microsoft.com/814a1105-0edc-4d1e-9f94-1c13152c0925">EMR_OFFSETCLIPRGN</a>
<a href="https://msdn.microsoft.com/91c0badc-bd26-418a-9cdb-3e70e7337021">EMR_PAINTRGN</a>
<a href="https://msdn.microsoft.com/f249b396-bf71-401b-b972-317d551fc9aa">EMR_PIE</a>
<a href="https://msdn.microsoft.com/3dd2ef54-af00-4d7e-b33f-c7c5160ae4f1">EMR_PIXELFORMAT</a>
<a href="https://msdn.microsoft.com/c802baa8-2f11-46e1-948c-f63c40e94266">EMR_PLGBLT</a>
<a href="https://msdn.microsoft.com/47a05287-8950-4277-b981-a19bff918bae">EMR_POLYBEZIER</a>
<a href="https://msdn.microsoft.com/ba1d4fad-44d7-438c-8e03-972d88c2780e">EMR_POLYBEZIER16</a>
<a href="https://msdn.microsoft.com/47a05287-8950-4277-b981-a19bff918bae">EMR_POLYBEZIERTO</a>
<a href="https://msdn.microsoft.com/ba1d4fad-44d7-438c-8e03-972d88c2780e">EMR_POLYBEZIERTO16</a>
<a href="https://msdn.microsoft.com/c75d19bf-a7e3-45db-9534-f089d4cec3eb">EMR_POLYDRAW</a>
<a href="https://msdn.microsoft.com/476c5a81-99fc-4e25-a761-b95bbf18b271">EMR_POLYDRAW16</a>
<a href="https://msdn.microsoft.com/47a05287-8950-4277-b981-a19bff918bae">EMR_POLYGON</a>
<a href="https://msdn.microsoft.com/ba1d4fad-44d7-438c-8e03-972d88c2780e">EMR_POLYGON16</a>
<a href="https://msdn.microsoft.com/47a05287-8950-4277-b981-a19bff918bae">EMR_POLYLINE</a>
<a href="https://msdn.microsoft.com/ba1d4fad-44d7-438c-8e03-972d88c2780e">EMR_POLYLINE16</a>
<a href="https://msdn.microsoft.com/47a05287-8950-4277-b981-a19bff918bae">EMR_POLYLINETO</a>
<a href="https://msdn.microsoft.com/ba1d4fad-44d7-438c-8e03-972d88c2780e">EMR_POLYLINETO16</a>
<a href="https://msdn.microsoft.com/442ad347-c064-4769-b43b-57d2e66e8b97">EMR_POLYPOLYGON</a>
<a href="https://msdn.microsoft.com/efdd4ed1-5c0e-43ae-980d-fe3a5e8d480f">EMR_POLYPOLYGON16</a>
<a href="https://msdn.microsoft.com/442ad347-c064-4769-b43b-57d2e66e8b97">EMR_POLYPOLYLINE</a>
<a href="https://msdn.microsoft.com/efdd4ed1-5c0e-43ae-980d-fe3a5e8d480f">EMR_POLYPOLYLINE16</a>
<a href="https://msdn.microsoft.com/9c1decdd-fe6f-4220-abba-7547ab5427ba">EMR_POLYTEXTOUTA</a>
<a href="https://msdn.microsoft.com/9c1decdd-fe6f-4220-abba-7547ab5427ba">EMR_POLYTEXTOUTW</a>
<a href="https://msdn.microsoft.com/ee9f57af-8d96-4b85-b8ab-4eb57e6c7c78">EMR_REALIZEPALETTE</a>
<a href="https://msdn.microsoft.com/1400f9d7-4ccd-4348-98f0-fccc78e06212">EMR_RECTANGLE</a>
<a href="https://msdn.microsoft.com/b9c31591-bf9f-44d9-8c9a-9682d29fc541">EMR_RESIZEPALETTE</a>
<a href="https://msdn.microsoft.com/c56767bf-a13e-4215-9005-6e543f3e5a0d">EMR_RESTOREDC</a>
<a href="https://msdn.microsoft.com/74caff9e-6882-4585-ad51-e83e4afb8454">EMR_ROUNDRECT</a>
<a href="https://msdn.microsoft.com/ee9f57af-8d96-4b85-b8ab-4eb57e6c7c78">EMR_SAVEDC</a>
<a href="https://msdn.microsoft.com/712e8b00-d9ab-4b23-aed4-d7aadd0cb3e1">EMR_SCALEVIEWPORTEXTEX</a>
<a href="https://msdn.microsoft.com/712e8b00-d9ab-4b23-aed4-d7aadd0cb3e1">EMR_SCALEWINDOWEXTEX</a>
<a href="https://msdn.microsoft.com/cae5eb68-169e-4439-9141-af93c8ff5ec6">EMR_SELECTCLIPPATH</a>
<a href="https://msdn.microsoft.com/02ec5839-3390-429b-8f0c-6f2e74393c8f">EMR_SELECTOBJECT</a>
<a href="https://msdn.microsoft.com/f83367c0-406a-4a5f-961f-8e5afe6707fd">EMR_SELECTPALETTE</a>
<a href="https://msdn.microsoft.com/d33d329f-7f66-4995-b80f-656c96ea105b">EMR_SETARCDIRECTION</a>
<a href="https://msdn.microsoft.com/9916fc79-cac0-4c46-8fa5-aeca3b7f2cf0">EMR_SETBKCOLOR</a>
<a href="https://msdn.microsoft.com/cae5eb68-169e-4439-9141-af93c8ff5ec6">EMR_SETBKMODE</a>
<a href="https://msdn.microsoft.com/4030c4c4-60be-43b7-855e-49d65ea482c1">EMR_SETBRUSHORGEX</a>
<a href="https://msdn.microsoft.com/d9f99f71-d102-484f-beb4-0d2de1070345">EMR_SETCOLORADJUSTMENT</a>
<a href="https://msdn.microsoft.com/c661b3cc-6b41-4157-acb4-f9083ab73851">EMR_SETCOLORSPACE</a>
<a href="https://msdn.microsoft.com/a87546e4-32ce-438d-9997-6d329f43303e">EMR_SETDIBITSTODEVICE</a>
<a href="https://msdn.microsoft.com/cae5eb68-169e-4439-9141-af93c8ff5ec6">EMR_SETICMMODE</a>
<a href="https://msdn.microsoft.com/2f43db1e-95eb-4812-9422-ddc9df634c15">EMR_SETICMPROFILEA</a>
<a href="https://msdn.microsoft.com/2f43db1e-95eb-4812-9422-ddc9df634c15">EMR_SETICMPROFILEW</a>
<a href="https://msdn.microsoft.com/cae5eb68-169e-4439-9141-af93c8ff5ec6">EMR_SETLAYOUT</a>
<a href="https://msdn.microsoft.com/cae5eb68-169e-4439-9141-af93c8ff5ec6">EMR_SETMAPMODE</a>
<a href="https://msdn.microsoft.com/d8a01e0a-6da9-43e2-9910-87503b5c851e">EMR_SETMAPPERFLAGS</a>
<a href="https://msdn.microsoft.com/ee9f57af-8d96-4b85-b8ab-4eb57e6c7c78">EMR_SETMETARGN</a>
<a href="https://msdn.microsoft.com/2d56eb0d-5417-464b-be6a-57e4654003e6">EMR_SETMITERLIMIT</a>
<a href="https://msdn.microsoft.com/df75567e-150f-4f88-b6ae-938b451a7b7d">EMR_SETPALETTEENTRIES</a>
<a href="https://msdn.microsoft.com/1487d788-c85a-4a58-a4c8-8abe198944b4">EMR_SETPIXELV</a>
<a href="https://msdn.microsoft.com/cae5eb68-169e-4439-9141-af93c8ff5ec6">EMR_SETPOLYFILLMODE</a>
<a href="https://msdn.microsoft.com/cae5eb68-169e-4439-9141-af93c8ff5ec6">EMR_SETROP2</a>
<a href="https://msdn.microsoft.com/cae5eb68-169e-4439-9141-af93c8ff5ec6">EMR_SETSTRETCHBLTMODE</a>
<a href="https://msdn.microsoft.com/cae5eb68-169e-4439-9141-af93c8ff5ec6">EMR_SETTEXTALIGN</a>
<a href="https://msdn.microsoft.com/9916fc79-cac0-4c46-8fa5-aeca3b7f2cf0">EMR_SETTEXTCOLOR</a>
<a href="https://msdn.microsoft.com/4030c4c4-60be-43b7-855e-49d65ea482c1">EMR_SETVIEWPORTEXTEX</a>
<a href="https://msdn.microsoft.com/df80b89a-67b2-4ab3-8ff8-f121f9eb88cd">EMR_SETVIEWPORTORGEX</a>
<a href="https://msdn.microsoft.com/4030c4c4-60be-43b7-855e-49d65ea482c1">EMR_SETWINDOWEXTEX</a>
<a href="https://msdn.microsoft.com/4030c4c4-60be-43b7-855e-49d65ea482c1">EMR_SETWINDOWORGEX</a>
<a href="https://msdn.microsoft.com/08e5e272-22b5-4097-a293-f5a1fd865edf">EMR_SETWORLDTRANSFORM</a>
<a href="https://msdn.microsoft.com/957b09d2-a706-4045-affb-fd530cd4fa3a">EMR_STRETCHBLT</a>
<a href="https://msdn.microsoft.com/aa104ffa-44ed-41f6-a1a7-23bbab68e16c">EMR_STRETCHDIBITS</a>
<a href="https://msdn.microsoft.com/9911e0fb-2e0d-4684-bff6-fc876ab8185d">EMR_STROKEANDFILLPATH</a>
<a href="https://msdn.microsoft.com/9911e0fb-2e0d-4684-bff6-fc876ab8185d">EMR_STROKEPATH</a>
<a href="https://msdn.microsoft.com/f343bc6a-87b8-4c6b-b2cb-3d7f2f515fc1">EMR_TRANSPARENTBLT</a>
<a href="https://msdn.microsoft.com/ee9f57af-8d96-4b85-b8ab-4eb57e6c7c78">EMR_WIDENPATH</a>

### -field nSize

The size of the record, in bytes. This member must be a multiple of four.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

