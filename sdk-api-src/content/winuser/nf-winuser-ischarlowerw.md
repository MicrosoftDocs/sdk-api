---
UID: NF:winuser.IsCharLowerW
title: IsCharLowerW
ms.date: 4/26/2019
ms.keywords: IsCharLowerW
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winuser.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-Core-Stringansi-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-user32-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
 - mfc120u.dll mfc140u.dll
api_name:
 - IsCharLowerW
---

## -description

Determines whether a character is lowercase. This determination is based on the semantics of the language selected by the user during setup or through Control Panel. 

## -parameters

### -param ch

Type: <b>TCHAR</b>

The character to be tested.

## -returns

Type: <b>BOOL</b>

If the character is lowercase, the return value is nonzero.

If the character is not lowercase, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks

## -see-also

<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-ischaruppera">IsCharUpper</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/strings">Strings</a>
 

