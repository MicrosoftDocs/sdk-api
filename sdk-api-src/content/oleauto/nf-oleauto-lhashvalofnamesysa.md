---
UID: NF:oleauto.LHashValOfNameSysA
title: LHashValOfNameSysA function
author: windows-sdk-content
description: Computes a hash value for the specified name.
old-location: automat\lhashvalofnamesysa.htm
old-project: automat
ms.assetid: 8a879533-c842-4ff7-b739-3f862281acaf
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: LHashValOfNameSysA, LHashValOfNameSysA function [Automation], _oa96_LHashValOfNameSysA, automat.lhashvalofnamesysa, oleauto/LHashValOfNameSysA
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	LHashValOfNameSysA
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LHashValOfNameSysA function


## -description


Computes a hash value for the specified name.


## -parameters




### -param syskind

The SYSKIND of the target operating system.




### -param lcid

The LCID for the string.




### -param szName

The string whose hash value is to be computed.



## -returns



A hash value that represents the specified name.




