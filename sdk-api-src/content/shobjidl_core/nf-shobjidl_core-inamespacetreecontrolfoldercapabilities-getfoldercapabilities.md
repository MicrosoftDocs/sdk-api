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

# INameSpaceTreeControlFolderCapabilities::GetFolderCapabilities


## -description


Gets a folder's capability to be filtered through the <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a> property key value and change notification registration status.


## -parameters




### -param nfcMask [in]

Type: <b><a href="https://msdn.microsoft.com/a5282277-85f5-494e-b994-efbf1116b519">NSTCFOLDERCAPABILITIES</a></b>

The capabilities for which this method should retrieve values. Specify one or both of the following:



#### NSTCFC_PINNEDITEMFILTERING (0x00000001)

0x00000001. The <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a> property exists on this folder and filtering based on that property value is supported.



#### NSTCFC_DELAY_REGISTER_NOTIFY (0x00000002)

0x00000002. Registration for change notifications is delayed until the folder is expanded in the navigation pane.


### -param pnfcValue






#### - pnstcfc [out]

Type: <b><a href="https://msdn.microsoft.com/a5282277-85f5-494e-b994-efbf1116b519">NSTCFOLDERCAPABILITIES</a>*</b>

Pointer to a value that, when this method returns successfully, receives the capabilities requested in <i>nfcMask</i>. Except in the case of NSTCFC_NONE, bit values in positions not specifically requested in <i>nfcMask</i> do not necessarily reflect the capabilities and should not be used.



#### NSTCFC_NONE (0x00000000)

0x00000000. The <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a> property does not exist on this folder. Filtering is not supported.



#### NSTCFC_PINNEDITEMFILTERING (0x00000001)

0x00000001. The <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a> property exists on this folder and filtering based on that property value is supported.



#### NSTCFC_DELAY_REGISTER_NOTIFY (0x00000002)

0x00000002. Registration for change notifications is delayed until the folder is expanded in the navigation pane.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



