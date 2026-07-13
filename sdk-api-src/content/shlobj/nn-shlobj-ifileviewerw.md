---
UID: NN:shlobj.IFileViewerW
title: IFileViewerW
description: Exposes methods that designate an interface that allows a registered file viewer to be notified when it must show or print a file. (Unicode)
helpviewer_keywords: ["IFileViewerW"]
old-location: 
tech.root: shell
ms.assetid: 659f6ff8-1797-4f66-b0cc-ca2b9ee15a3a
ms.date: 01/30/2019
ms.keywords: IFileViewerW
targetos: Windows
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: shlobj.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
f1_keywords:
 - IFileViewerW
 - shlobj/IFileViewerW
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - shlobj.h
api_name:
 - IFileViewerW
---

## -description

Exposes methods that designate an interface that allows a registered file viewer to be notified when it must show or print a file.

## -remarks

File viewers are not supported by Windows 2000 and later systems.

Implement this interface to provide a means for your registered file types to be viewed and/or printed.

You do not typically use this interface. The Shell calls the interface when the user chooses the **Quick View** command from a file's shortcut menu and the file is a type that the file viewer recognizes.



> [!NOTE]
> The shlobj.h header defines IFileViewer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

