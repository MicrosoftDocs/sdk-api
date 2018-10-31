---
UID: NF:oleauto.GetAltMonthNames
title: GetAltMonthNames function
author: windows-sdk-content
description: Retrieves the secondary (alternate) month names.
old-location: automat\getaltmonthnames.htm
tech.root: automat
ms.assetid: dfde73f2-edb9-4ab9-9394-d859e61a6db8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetAltMonthNames, GetAltMonthNames function [Automation], _oa96_GetAltMonthNames, automat.getaltmonthnames, oleauto/GetAltMonthNames
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - GetAltMonthNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetAltMonthNames function


## -description


Retrieves the secondary (alternate) month names.


## -parameters




### -param lcid [in]

The locale identifier to be used in retrieving the alternate month names.


### -param prgp [out]

An array of pointers to strings containing the alternate month names.


## -returns



The function returns TRUE on success and FALSE otherwise.




## -remarks



Useful for Hijri, Polish and Russian alternate month names.



