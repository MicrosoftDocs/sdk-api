---
UID: NF:wiautil.wiauGetValidFormats
title: wiauGetValidFormats function
author: windows-driver-content
description: The wiauGetValidFormats function calls the IWiaMiniDrv::drvGetWiaFormatInfo method and makes a list of valid formats, using a specified tymed value.
old-location: image\wiaugetvalidformats.htm
old-project: image
ms.assetid: 8bf1d76a-2e5b-4e9a-85fc-187fea72d38c
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaugetvalidformats, wiauFncs_f311862b-03fe-4fe6-8b30-46cd9a53513b.xml, wiauGetValidFormats, wiauGetValidFormats function [Imaging Devices], wiautil/wiauGetValidFormats
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
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
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiautil.h
api_name:
-	wiauGetValidFormats
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauGetValidFormats function


## -description


The <b>wiauGetValidFormats</b> function calls the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543986">IWiaMiniDrv::drvGetWiaFormatInfo</a> method and makes a list of valid formats, using a specified tymed value.


## -parameters




### -param pDrv [in]

Points to the WIA minidriver object. This parameter should be set to <b>this</b>.


### -param pWiasContext [in]

Pointer to a WIA item context.


### -param TymedValue

Specifies the tymed value to search for.


### -param pNumFormats [out]

Pointer to a memory location that receives the number of formats.


### -param ppFormatArray [out]

Pointer to a memory location that receives the address of the array of format GUIDs.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error.




## -remarks



The caller of this function is responsible for freeing the format array, using the <b>delete[]</b> operator.



