---
UID: NF:oleauto.SafeArrayGetElemsize
title: SafeArrayGetElemsize function
author: windows-sdk-content
description: Gets the size of an element.
old-location: automat\safearraygetelemsize.htm
old-project: automat
ms.assetid: 27bd4a3f-0e9d-45f7-ad7c-0c0b59579dd0
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: SafeArrayGetElemsize, SafeArrayGetElemsize function [Automation], _oa96_SafeArrayGetElemsize, automat.safearraygetelemsize, oleauto/SafeArrayGetElemsize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayGetElemsize
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# SafeArrayGetElemsize function


## -description


Gets the size of an element.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.


## -returns



The size of an element in a safe array, in bytes.



