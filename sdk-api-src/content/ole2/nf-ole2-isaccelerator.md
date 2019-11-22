---
UID: NF:ole2.IsAccelerator
title: IsAccelerator function (ole2.h)

description: Determines whether the specified keystroke maps to an accelerator in the specified accelerator table.
old-location: com\isaccelerator.htm
tech.root: com
ms.assetid: 2d09f81a-b422-4379-89c8-d50992ebb24c

ms.date: 12/05/2018
ms.keywords: IsAccelerator, IsAccelerator function [COM], _com_IsAccelerator, com.isaccelerator, ole2/IsAccelerator
ms.topic: function
f1_keywords: 
 - "ole2/IsAccelerator"
dev_langs:
 - c++
req.header: ole2.h
req.include-header: 
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - IsAccelerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsAccelerator function


## -description


Determines whether the specified keystroke maps to an accelerator in the specified accelerator table.


## -parameters




### -param hAccel [in]

A handle to the accelerator table.


### -param cAccelEntries [in]

The number of entries in the accelerator table.


### -param lpMsg [in]

A pointer to the keystroke message to be translated.


### -param lpwCmd [out]

A pointer to a variable  to receive the corresponding command identifier if there is an accelerator for the keystroke. This parameter may be <b>NULL</b>.


## -returns



If the message is for the object application, the return value is <b>TRUE</b>. If the message is not for the object and should be forwarded to the container, the return value is <b>FALSE</b>.




## -remarks



While an object is active in-place, the object always has first chance to translate the keystrokes into accelerators. If the keystroke corresponds to one of its accelerators, the object must not call the <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a> function â€” even if its call to the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbasepropertypage-translateaccelerator">TranslateAccelerator</a> function fails. Failure to process keystrokes in this manner can lead to inconsistent behavior.

If the keystroke is not one of the object's accelerators, then the object must call <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a> to let the container try its accelerator translation.

The object's server can call <b>IsAccelerator</b> to determine if the accelerator message belongs to it. Some servers do accelerator translation on their own and do not call <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbasepropertypage-translateaccelerator">TranslateAccelerator</a>. Those applications will not call <b>IsAccelerator</b>, because they already have the information.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbasepropertypage-translateaccelerator">TranslateAccelerator</a>
 

 

