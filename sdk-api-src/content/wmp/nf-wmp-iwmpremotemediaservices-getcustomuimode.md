---
UID: NF:wmp.IWMPRemoteMediaServices.GetCustomUIMode
title: IWMPRemoteMediaServices::GetCustomUIMode
author: windows-sdk-content
description: The GetCustomUIMode method is called by Windows Media Player to retrieve the location of a skin file to apply to the Windows Media Player control.
old-location: wmp\iwmpremotemediaservices_getcustomuimode.htm
old-project: WMP
ms.assetid: 892c2513-9ca2-48fe-b745-0fdc0f445871
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCustomUIMode, GetCustomUIMode method [Windows Media Player], GetCustomUIMode method [Windows Media Player],IWMPRemoteMediaServices interface, IWMPRemoteMediaServices interface [Windows Media Player],GetCustomUIMode method, IWMPRemoteMediaServices.GetCustomUIMode, IWMPRemoteMediaServices::GetCustomUIMode, IWMPRemoteMediaServicesGetCustomUIMode, wmp.iwmpremotemediaservices_getcustomuimode, wmp/IWMPRemoteMediaServices::GetCustomUIMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPRemoteMediaServices.GetCustomUIMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPRemoteMediaServices::GetCustomUIMode


## -description



The <b>GetCustomUIMode</b> method is called by Windows Media Player to retrieve the location of a skin file to apply to the Windows Media Player control.




## -parameters




### -param pbstrFile [out]

Pointer to a <b>BSTR</b> containing the location of the skin file.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>
 




## -remarks



This method allows you to customize the user interface of the embedded control by using Windows Media Player skin technology. Skins used in this way can communicate with the host of the control through a scriptable object retrieved automatically by Windows Media Player through the <b>IWMPRemoteMediaServices::GetScriptableObject</b> method.

To apply a skin file to the embedded control, you must call <b>IWMPPlayer.put_uiMode</b> with a value of "custom". Your implementation of <b>GetCustomUIMode</b> must also return a value of "file://" followed by the path and file name of a skin definition file located on the local computer.

The embedded Windows Media Player control does not have to be remoted to use this method.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/594a614a-8da1-4ef0-a6af-01284fb48ef7">IWMPRemoteMediaServices Interface</a>



<a href="https://msdn.microsoft.com/c2e313fd-cbf6-4b0f-8eb0-1097af53e77a">IWMPRemoteMediaServices::GetScriptableObject</a>



<a href="https://msdn.microsoft.com/0381e0e4-c686-4ab4-b947-b883b6f4e06e">Using Skins with the Windows Media Player Control</a>
 

 

