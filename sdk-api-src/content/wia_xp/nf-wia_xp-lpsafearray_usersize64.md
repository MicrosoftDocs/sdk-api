---
UID: NF:wia_xp.LPSAFEARRAY_UserSize64
title: LPSAFEARRAY_UserSize64 function
author: windows-sdk-content
description: Calculates the wire size of the SAFEARRAY object, and gets its handle and data.
old-location: automat\lpsafearray_usersize64.htm
old-project: automat
ms.assetid: 5F41D197-027E-4640-833A-4F6239F0DFB0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LPSAFEARRAY_UserSize64, LPSAFEARRAY_UserSize64 function [Automation], automat.lpsafearray_usersize64, wia_xp/LPSAFEARRAY_UserSize64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wia_xp.h
req.include-header: Propidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - LPSAFEARRAY_UserSize64
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LPSAFEARRAY_UserSize64 function


## -description


Calculates the wire size of the <a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> object, and gets its handle and data.


## -parameters




### -param

TBD




#### - [in]

The data used by RPC.


#### - Offset [in]

Sets the buffer offset so that the <a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> object is properly aligned when it is marshaled to the buffer.


#### - ppSafeArray [in]

The safe array that contains the data to marshal.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.



