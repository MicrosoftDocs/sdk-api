---
UID: NS:mfobjects._MFVIDEOFORMAT
title: "_MFVIDEOFORMAT"
author: windows-sdk-content
description: Describes a video format.
old-location: mf\mfvideoformat.htm
tech.root: medfound
ms.assetid: 7fbc4a35-117c-4f0c-9e9b-ff44e30a1618
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 7fbc4a35-117c-4f0c-9e9b-ff44e30a1618, MFVIDEOFORMAT, MFVIDEOFORMAT structure [Media Foundation], _MFVIDEOFORMAT, mf.mfvideoformat, mfobjects/MFVIDEOFORMAT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mfobjects.h
req.include-header: Mfidl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFVIDEOFORMAT
product: Windows
targetos: Windows
req.typenames: MFVIDEOFORMAT
req.redist: 
---

# _MFVIDEOFORMAT structure


## -description



Describes a video format.




## -struct-fields




### -field dwSize

Size of the structure, in bytes. This value includes the size of the palette entries that may appear after the <b>surfaceInfo</b> member.


### -field videoInfo


<a href="https://msdn.microsoft.com/746fd84f-58f8-42ab-bcf7-8fd18dcd02af">MFVideoInfo</a> structure. This structure contains information that applies to both compressed and uncompressed formats.


### -field guidFormat

Video subtype. See <a href="https://msdn.microsoft.com/7dfd85e6-936e-4b78-a2cb-a5d59153e1c4">Video Subtype GUIDs</a>.


### -field compressedInfo


<a href="https://msdn.microsoft.com/fe9aa287-33e9-4413-8bc5-0e7b2da1112e">MFVideoCompressedInfo</a> structure. This structure contains information that applies only to compressed formats.


### -field surfaceInfo


<a href="https://msdn.microsoft.com/b48099a2-8427-496c-9a60-ace5b89d81e9">MFVideoSurfaceInfo</a> structure. This structure contains information that applies only to uncompressed formats.


## -remarks



Applications should avoid using this structure. Instead, it is recommended that applications use attributes to describe the video format. For a list of media type attributes, see <a href="https://msdn.microsoft.com/e84ba3f6-4857-4340-baca-5847650ea7b8">Media Type Attributes</a>. With attributes, you can set just the format information that you know, which is easier (and more likely to be accurate) than trying to fill in complete format information for the <b>MFVIDEOFORMAT</b> structure.

To initialize a media type object from an <b>MFVIDEOFORMAT</b> structure, call <a href="https://msdn.microsoft.com/45400b67-df81-4fae-a24d-80020eb07151">MFInitMediaTypeFromMFVideoFormat</a>.

You can use the <b>MFVIDEOFORMAT</b> structure as the format block for a DirectShow media type. Set the format GUID to FORMAT_MFVideoFormat.




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

