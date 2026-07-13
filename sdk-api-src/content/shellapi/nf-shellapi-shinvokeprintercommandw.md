---
UID: NF:shellapi.SHInvokePrinterCommandW
title: SHInvokePrinterCommandW function (shellapi.h)
description: Executes a command on a printer object. (Unicode)
helpviewer_keywords: ["PRINTACTION_DOCUMENTDEFAULTS", "PRINTACTION_NETINSTALL", "PRINTACTION_NETINSTALLLINK", "PRINTACTION_OPEN", "PRINTACTION_OPENNETPRN", "PRINTACTION_PROPERTIES", "PRINTACTION_SERVERPROPERTIES", "PRINTACTION_TESTPAGE", "SHInvokePrinterCommand", "SHInvokePrinterCommand function [Windows Shell]", "SHInvokePrinterCommandW", "_win32_SHInvokePrinterCommand", "shell.SHInvokePrinterCommand", "shellapi/SHInvokePrinterCommand", "shellapi/SHInvokePrinterCommandW"]
old-location: shell\SHInvokePrinterCommand.htm
tech.root: shell
ms.assetid: 32a5802f-cef7-4dbd-affd-82285fe97a8c
ms.date: 12/05/2018
ms.keywords: PRINTACTION_DOCUMENTDEFAULTS, PRINTACTION_NETINSTALL, PRINTACTION_NETINSTALLLINK, PRINTACTION_OPEN, PRINTACTION_OPENNETPRN, PRINTACTION_PROPERTIES, PRINTACTION_SERVERPROPERTIES, PRINTACTION_TESTPAGE, SHInvokePrinterCommand, SHInvokePrinterCommand function [Windows Shell], SHInvokePrinterCommandA, SHInvokePrinterCommandW, _win32_SHInvokePrinterCommand, shell.SHInvokePrinterCommand, shellapi/SHInvokePrinterCommand, shellapi/SHInvokePrinterCommandA, shellapi/SHInvokePrinterCommandW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHInvokePrinterCommandW (Unicode) and SHInvokePrinterCommandA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHInvokePrinterCommandW
 - shellapi/SHInvokePrinterCommandW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHInvokePrinterCommand
 - SHInvokePrinterCommandA
 - SHInvokePrinterCommandW
---

# SHInvokePrinterCommandW function


## -description

Executes a command on a printer object.
            
            
<div class="alert"><b>Note</b>  This function has been deprecated as of Windows Vista. It is recommended that, in its place, you invoke verbs on printers through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> or <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a>.</div><div> </div>

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

The handle of the parent window of any windows or dialog boxes that are created during the operation.

### -param uAction

Type: <b>UINT</b>

The type of printer operation to perform. One of the following values:





#### PRINTACTION_OPEN (0)

0x0. Open the printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored. 



#### PRINTACTION_PROPERTIES (1)

0x1. Display the property pages for the printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter can be <b>NULL</b> or can name a specific property sheet to display, either by name or number. If the high <b>WORD</b> of <i>lpBuf2</i> is nonzero, it is assumed that this parameter is a pointer to a buffer that contains the name of the sheet to open. Otherwise, <i>lpBuf2</i> is seen as the zero-based index of the property sheet to open.



#### PRINTACTION_NETINSTALL (2)

0x2. Install the network printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored.



#### PRINTACTION_NETINSTALLLINK (3)

0x3. Create a shortcut to the network printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter specifies the drive and path of the folder in which to create the shortcut. The network printer must already have been installed on the local computer.



#### PRINTACTION_TESTPAGE (4)

0x4. Print a test page on the printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored.



#### PRINTACTION_OPENNETPRN (5)

0x5. Open the network printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored.



#### PRINTACTION_DOCUMENTDEFAULTS (6)

0x6. Display the default document properties for the printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored. 



#### PRINTACTION_SERVERPROPERTIES (7)

0x7. Display the properties for the printer server specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored.

### -param lpBuf1 [in]

Type: <b>LPCTSTR</b>

Pointer to a null-terminated string that contains additional information for the printer command. The information contained in this parameter depends upon the value of <i>uAction</i>.

### -param lpBuf2 [in, optional]

Type: <b>LPCTSTR</b>

Pointer to a null-terminated string that contains additional information for the printer command. The information contained in this parameter depends upon the value of <i>uAction</i>.

### -param fModal

Type: <b>BOOL</b>

<b>TRUE</b> to specify that <b>SHInvokePrinterCommand</b> should not return until the command is completed; <b>FALSE</b> if the function should return as soon as the command is initialized.


##### - uAction.PRINTACTION_DOCUMENTDEFAULTS (6)

0x6. Display the default document properties for the printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored. 


##### - uAction.PRINTACTION_NETINSTALL (2)

0x2. Install the network printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored.


##### - uAction.PRINTACTION_NETINSTALLLINK (3)

0x3. Create a shortcut to the network printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter specifies the drive and path of the folder in which to create the shortcut. The network printer must already have been installed on the local computer.


##### - uAction.PRINTACTION_OPEN (0)

0x0. Open the printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored. 


##### - uAction.PRINTACTION_OPENNETPRN (5)

0x5. Open the network printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored.


##### - uAction.PRINTACTION_PROPERTIES (1)

0x1. Display the property pages for the printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter can be <b>NULL</b> or can name a specific property sheet to display, either by name or number. If the high <b>WORD</b> of <i>lpBuf2</i> is nonzero, it is assumed that this parameter is a pointer to a buffer that contains the name of the sheet to open. Otherwise, <i>lpBuf2</i> is seen as the zero-based index of the property sheet to open.


##### - uAction.PRINTACTION_SERVERPROPERTIES (7)

0x7. Display the properties for the printer server specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored.


##### - uAction.PRINTACTION_TESTPAGE (4)

0x4. Print a test page on the printer specified by <i>lpBuf1</i>. The <i>lpBuf2</i> parameter is ignored.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.

## -remarks

When a printer name is specified by <i>lpBuf1</i>, the name can either be the name of a local printer or the server and share name of a network printer. When specifying a network printer name, the name must be specified in this format: 


```
"\\<server><shared printer name>"
```


This function is implemented in <a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Shell versions 4.71</a> and later. In order to maintain backward compatibility with previous Shell versions, this function should not be used explicitly. Instead, the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions should be used to obtain the function address.




> [!NOTE]
> The shellapi.h header defines SHInvokePrinterCommand as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
