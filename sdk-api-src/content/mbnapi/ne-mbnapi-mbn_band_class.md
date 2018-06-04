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

# MBN_BAND_CLASS enumeration


## -description


The <b>MBN_BAND_CLASS</b> enumerated type defines the frequency band classes.


## -enum-fields




### -field MBN_BAND_CLASS_NONE

Unknown band class.


### -field MBN_BAND_CLASS_0

Band class 0.


### -field MBN_BAND_CLASS_I

Band class 1.


### -field MBN_BAND_CLASS_II

Band class 2.


### -field MBN_BAND_CLASS_III

Band class 3.


### -field MBN_BAND_CLASS_IV

Band class 4.


### -field MBN_BAND_CLASS_V

Band class 5.


### -field MBN_BAND_CLASS_VI

Band class 6.


### -field MBN_BAND_CLASS_VII

Band class 7.


### -field MBN_BAND_CLASS_VIII

Band class 8.


### -field MBN_BAND_CLASS_IX

Band class 9.


### -field MBN_BAND_CLASS_X

Band class 10.


### -field MBN_BAND_CLASS_XI

Band class 11.


### -field MBN_BAND_CLASS_XII

Band class 12.


### -field MBN_BAND_CLASS_XIII

Band class 13.


### -field MBN_BAND_CLASS_XIV

Band class 14.


### -field MBN_BAND_CLASS_XV

Band class 15.


### -field MBN_BAND_CLASS_XVI

Band class 16.


### -field MBN_BAND_CLASS_XVII

Band class 17.


### -field MBN_BAND_CLASS_CUSTOM

Custom band class.


## -remarks



These  values are used by the <b>gsmBandClass</b> and <b>cdmaBandClass</b> members of the <a href="https://msdn.microsoft.com/faee7f53-b465-4240-b163-ce88fae764df">MBN_INTERFACE_CAPS</a> structure.  The meanings are dependent upon which member is using them and are detailed in the structure documentation



