---
UID: NF:wtypesbase.OLESTR
title: OLESTR macro
author: windows-driver-content
description: Transforms string literals into Unicode strings.
old-location: com\olestr_macro.htm
old-project: com
ms.assetid: bf3341a0-5b1d-479b-998d-a61bb945e0c3
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: OLESTR, OLESTR macro [COM], _com_OLESTR, com.olestr, com.olestr_macro, wtypesbase/OLESTR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wtypesbase.h
req.include-header: WTypes.h
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
req.typenames: MSHLFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wtypesbase.h
api_name:
-	OLESTR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OLESTR macro


## -description


Transforms string literals into Unicode strings.


## -parameters




### -param str

A string literal.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define OLESTR(str) L##str
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

