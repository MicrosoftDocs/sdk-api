---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _DETAILSINFO structure


## -description


Contains detail information for a Shell folder item. Used with the <a href="https://msdn.microsoft.com/46a81a7b-527c-4d41-8d25-ce65fd87416e">SFVM_GETDETAILSOF</a> notification.


## -struct-fields




### -field pidl

Type: <b>PCUITEMID_CHILD</b>

PIDL of the item whose details are being retrieved.


### -field fmt

Type: <b>int</b>

The alignment of the column heading and the subitem text in the column. This member can be one of the following values. Note that the alignment of the leftmost column is always left-justified and cannot be changed.



#### LVCFMT_CENTER

Text is centered.



#### LVCFMT_COL_HAS_IMAGES

Header item contains an image in the image list.



#### LVCFMT_LEFT

Text is left-aligned.



#### LVCFMT_RIGHT

Text is right-aligned.


### -field cxChar

Type: <b>int</b>

The number of average-sized characters in the heading.


### -field str

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a></b>

An <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure that includes a string containing the requested detail. To convert this structure to a string, use <a href="https://msdn.microsoft.com/89dab3ee-e9f8-499a-97ec-6fe732315891">StrRetToBuf</a> or <a href="https://msdn.microsoft.com/03b0dffb-8ef7-41da-9773-81ed55275802">StrRetToStr</a>.


### -field iImage

Type: <b>int</b>

The index of an icon in the Shell image list that is displayed in the view.

