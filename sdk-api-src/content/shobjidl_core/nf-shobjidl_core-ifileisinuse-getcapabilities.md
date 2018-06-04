---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



