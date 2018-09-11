---
UID: NE:strmif.tagDVD_SUBPICTURE_LANG_EXT
title: tagDVD_SUBPICTURE_LANG_EXT
author: windows-sdk-content
description: Defines the possible language extensions in a specified subpicture stream.
old-location: dshow\dvd_subpicture_lang_ext.htm
tech.root: DirectShow
ms.assetid: 314c6187-a475-44c9-b22a-b168211fceb3
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: DVD_SP_EXT_CC_Big, DVD_SP_EXT_CC_Children, DVD_SP_EXT_CC_Normal, DVD_SP_EXT_Caption_Big, DVD_SP_EXT_Caption_Children, DVD_SP_EXT_Caption_Normal, DVD_SP_EXT_DirectorComments_Big, DVD_SP_EXT_DirectorComments_Children, DVD_SP_EXT_DirectorComments_Normal, DVD_SP_EXT_Forced, DVD_SP_EXT_NotSpecified, DVD_SUBPICTURE_LANG_EXT, DVD_SUBPICTURE_LANG_EXT , DVD_SUBPICTURE_LANG_EXT enumeration [DirectShow], DVD_SUBPICTURE_LANG_EXTEnumeration, dshow.dvd_subpicture_lang_ext, strmif/DVD_SP_EXT_CC_Big, strmif/DVD_SP_EXT_CC_Children, strmif/DVD_SP_EXT_CC_Normal, strmif/DVD_SP_EXT_Caption_Big, strmif/DVD_SP_EXT_Caption_Children, strmif/DVD_SP_EXT_Caption_Normal, strmif/DVD_SP_EXT_DirectorComments_Big, strmif/DVD_SP_EXT_DirectorComments_Children, strmif/DVD_SP_EXT_DirectorComments_Normal, strmif/DVD_SP_EXT_Forced, strmif/DVD_SP_EXT_NotSpecified, strmif/DVD_SUBPICTURE_LANG_EXT, tagDVD_SUBPICTURE_LANG_EXT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_SUBPICTURE_LANG_EXT
product: Windows
targetos: Windows
req.typenames: DVD_SUBPICTURE_LANG_EXT
req.redist: 
---

# tagDVD_SUBPICTURE_LANG_EXT enumeration


## -description



Defines the possible language extensions in a specified subpicture stream.




## -enum-fields




### -field DVD_SP_EXT_NotSpecified

Indicates that no language extensions are present.


### -field DVD_SP_EXT_Caption_Normal

Indicates that the specified stream contains normal captions.


### -field DVD_SP_EXT_Caption_Big

Indicates that the specified stream contains big captions.


### -field DVD_SP_EXT_Caption_Children

Indicates that the specified stream contains captions for children.


### -field DVD_SP_EXT_CC_Normal

Indicates that the specified stream contains normal closed captions.


### -field DVD_SP_EXT_CC_Big

Indicates that the specified stream contains big closed captions.


### -field DVD_SP_EXT_CC_Children

Indicates that the specified stream contains closed captions for children.


### -field DVD_SP_EXT_Forced

Indicates that the subpicture stream is forcedly activated, meaning that the application will not be able to turn it off.


### -field DVD_SP_EXT_DirectorComments_Normal

Indicates that the specified stream contains normal-sized director's comments.


### -field DVD_SP_EXT_DirectorComments_Big

Indicates that the specified stream contains large-sized director's comments.


### -field DVD_SP_EXT_DirectorComments_Children

Indicates that the specified stream contains director's comments for children. 
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/f49698cd-cc83-4f05-991d-2b3bba77c33a">IDvdControl2::SelectDefaultSubpictureLanguage</a>



<a href="https://msdn.microsoft.com/ada423a5-90ef-48e1-80fa-04d0a24da8f7">IDvdInfo2::GetDefaultSubpictureLanguage</a>
 

 

