---
UID: NF:shobjidl_core.IFileIsInUse.GetCapabilities
title: IFileIsInUse::GetCapabilities
author: windows-sdk-content
description: Determines whether the file can be closed and whether the UI is capable of switching to the window of the application that is using the file.
old-location: shell\IFileIsInUse_GetCapabilities.htm
tech.root: shell
ms.assetid: d2ce674a-4c06-401d-bfb0-bc2a086ef89c
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetCapabilities, GetCapabilities method [Windows Shell], GetCapabilities method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],GetCapabilities method, IFileIsInUse.GetCapabilities, IFileIsInUse::GetCapabilities, OF_CAP_CANCLOSE, OF_CAP_CANSWITCHTO, _shell_IFileIsInUse_GetCapabilities, shell.IFileIsInUse_GetCapabilities, shobjidl_core/IFileIsInUse::GetCapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileIsInUse.GetCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileIsInUse::GetCapabilities


## -description


Determines whether the file can be closed and whether the UI is capable of switching to the window of the application that is using the file.


## -parameters




### -param pdwCapFlags [out]

Type: <b>DWORD*</b>

A pointer to a value that, when this method returns successfully, receives the capability flags. One or both of the following values:



#### OF_CAP_CANSWITCHTO (0x0001)

0x0001. The UI can switch to the top-level window of the application that is using the file.



#### OF_CAP_CANCLOSE (0x0002)

0x0002. The file can be closed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The capabilities returned by this method can be used in the composition of the dialog box presented to the user that informs them of the sharing conflict. For instance, if the OF_CAP_CANSWITCHTO flag is retrieved, a button can be added to the dialog box that will switch the user to the conflicting application window (based on the <b>HWND</b> information retrieved by <a href="https://msdn.microsoft.com/b4223cb0-2027-4073-9558-99ae27f4e52a">IFileIsInUse::GetSwitchToHWND</a>) so that the user can address the situation as they see fit. If the OF_CAP_CANCLOSE flag is retrieved, the dialog box can present a <b>Close</b> button that calls the <a href="https://msdn.microsoft.com/27338e5a-b303-4b72-b316-3059ec6f1698">CloseFile</a> method.



