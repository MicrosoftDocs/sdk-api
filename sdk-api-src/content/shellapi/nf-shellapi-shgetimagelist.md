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

# SHGetImageList function


## -description


Retrieves an image list.


## -parameters




### -param iImageList [in]

Type: <b>int</b>

The image type contained in the list. One of the following values:



#### SHIL_LARGE (0x0)

0x0. The image size is normally 32x32 pixels. However, if the <b>Use large icons</b> option is selected from the <b>Effects</b> section of the <b>Appearance</b> tab in <b>Display Properties</b>, the image is 48x48 pixels.



#### SHIL_SMALL (0x1)

0x1. These images are the Shell standard small icon size of 16x16, but the size can be customized by the user.



#### SHIL_EXTRALARGE (0x2)

0x2. These images are the Shell standard extra-large icon size. This is typically 48x48, but the size can be customized by the user.



#### SHIL_SYSSMALL (0x3)

0x3. These images are the size specified by <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> called with <b>SM_CXSMICON</b> and <b>GetSystemMetrics</b> called with <b>SM_CYSMICON</b>.



#### SHIL_JUMBO (0x4)

0x4. <b>Windows Vista and later.</b> The image is normally 256x256 pixels.



#### SHIL_LAST

The largest valid flag value, for validation purposes.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the image list interface identifier, normally IID_IImageList.


### -param ppvObj

TBD




#### - ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/02e397a4-22fa-49fb-8103-376aa5ebc77a">IImageList</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/02e397a4-22fa-49fb-8103-376aa5ebc77a">IImageList</a> pointer type, such as that returned in the <i>ppv</i> parameter, can be cast as an <b>HIMAGELIST</b> as needed; for example, for use in a list view. Conversely, an <b>HIMAGELIST</b> can be cast as a pointer to an <b>IImageList</b>.

As of Windows Vista, <b>SHIL_SMALL</b>, <b>SHIL_LARGE</b>, and <b>SHIL_EXTRALARGE</b> scale with dots per inch (dpi) if the process is marked as dpi-aware. To set these types to be dpi-aware, call <a href="https://msdn.microsoft.com/d9344028-3429-400c-8872-6545757c0494">SetProcessDPIAware</a>. <b>SHIL_JUMBO</b> is fixed at 256 pixels regardless of the dpi-aware setting.




## -see-also




<a href="https://msdn.microsoft.com/4e661326-157e-4c75-86df-cd213e01c3e5">FileIconInit</a>
 

 

