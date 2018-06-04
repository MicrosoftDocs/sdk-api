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

# URLAssociationDialogA function


## -description


Invokes the unregistered URL protocol dialog box. This dialog box allows the user to select an application to associate with a previously unknown protocol.
<div class="alert"><b>Note</b>  Windows XP Service Pack 2 (SP2) or later: This function is no longer supported.</div><div> </div>

## -parameters




### -param hwndParent

Type: <b>HWND</b>

A handle to the parent window.


### -param dwInFlags

Type: <b>DWORD</b>

The bit flags that specify the behavior of the function. This value can be a combination of the following:



#### URLASSOCDLG_FL_USE_DEFAULT_NAME

Use the default file name (that is, "Internet Shortcut").



#### URLASSOCDLG_FL_REGISTER_ASSOC

Register the selected application as the handler for the protocol specified in <i>pcszURL</i>. The application is registered only if this flag is set and the user indicates that a persistent association is desired.


### -param pcszFile

Type: <b>PTCSTR</b>

The address of a constant zero-terminated string that contains the file name to associate with the URLs protocol.


### -param pcszURL

Type: <b>PTCSTR</b>

The address of a constant zero-terminated string that contains the URL with an unknown protocol.


### -param pszAppBuf [out]

Type: <b>PTSTR</b>

The address of a buffer that receives the path of the application specified by the user.


### -param ucAppBufLen

Type: <b>UINT</b>

The size of <i>pszAppBuf</i>, in characters.


## -returns



Type: <b>HRESULT</b>

<div class="alert"><b>Note</b>  As of Windows XP SP2, this function not supported and returns E_NOTIMPL in all situations.</div>
<div> </div>
In supported systems, returns S_OK if the application is registered with the URL protocol, or S_FALSE if nothing is registered. For example, the function returns S_FALSE when the user elects to perform a one-time execution via the selected application.



