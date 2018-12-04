---
UID: NF:wmp.IWMPRemoteMediaServices.GetScriptableObject
title: IWMPRemoteMediaServices::GetScriptableObject
author: windows-sdk-content
description: The GetScriptableObject method is called by Windows Media Player to retrieve a name and interface pointer for an object that can be called from the script code within a skin.
old-location: wmp\iwmpremotemediaservices_getscriptableobject.htm
tech.root: WMP
ms.assetid: c2e313fd-cbf6-4b0f-8eb0-1097af53e77a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetScriptableObject, GetScriptableObject method [Windows Media Player], GetScriptableObject method [Windows Media Player],IWMPRemoteMediaServices interface, IWMPRemoteMediaServices interface [Windows Media Player],GetScriptableObject method, IWMPRemoteMediaServices.GetScriptableObject, IWMPRemoteMediaServices::GetScriptableObject, IWMPRemoteMediaServicesGetScriptableObject, wmp.iwmpremotemediaservices_getscriptableobject, wmp/IWMPRemoteMediaServices::GetScriptableObject
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPRemoteMediaServices.GetScriptableObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPRemoteMediaServices::GetScriptableObject


## -description



The <b>GetScriptableObject</b> method is called by Windows Media Player to retrieve a name and interface pointer for an object that can be called from the script code within a skin.




## -parameters




### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name of the scriptable object.


### -param ppDispatch [out]

Pointer to a pointer to the <b>IDispatch</b> interface of the scriptable object.


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



The user interface of an embedded control can be customized by using Windows Media Player skin technology. You must specify a skin file location by using the <b>IWMPRemoteMediaServices::GetCustomUIMode</b> method. Skins used in this way can communicate with the host of the control through a scriptable object retrieved automatically by Windows Media Player through the <b>IWMPRemoteMediaServices::GetScriptableObject</b> method.

The embedded Windows Media Player control does not have to be remoted to use this method.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/594a614a-8da1-4ef0-a6af-01284fb48ef7">IWMPRemoteMediaServices Interface</a>



<a href="https://msdn.microsoft.com/892c2513-9ca2-48fe-b745-0fdc0f445871">IWMPRemoteMediaServices::GetCustomUIMode</a>



<a href="https://msdn.microsoft.com/0381e0e4-c686-4ab4-b947-b883b6f4e06e">Using Skins with the Windows Media Player Control</a>
 

 

