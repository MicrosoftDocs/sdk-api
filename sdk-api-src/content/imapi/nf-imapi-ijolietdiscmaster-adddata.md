---
UID: NF:imapi.IJolietDiscMaster.AddData
title: IJolietDiscMaster::AddData
author: windows-sdk-content
description: Adds the contents of a root storage to the staged image file. This storage will be enumerated to place all substorages and streams in the root file system of the stage image file. Substorages become folders and streams become files.
old-location: imapi\ijolietdiscmaster_adddata.htm
tech.root: imapi
ms.assetid: 91517103-71c5-450c-9d93-584f94cd2c45
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddData, AddData method [IMAPI], AddData method [IMAPI],IJolietDiscMaster interface, IJolietDiscMaster interface [IMAPI],AddData method, IJolietDiscMaster.AddData, IJolietDiscMaster::AddData, _win32_ijolietdiscmaster_adddata, base.ijolietdiscmaster_adddata, imapi.ijolietdiscmaster_adddata, imapi/IJolietDiscMaster::AddData
ms.topic: method
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IJolietDiscMaster.AddData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IJolietDiscMaster::AddData


## -description


Adds the contents of a root storage to the staged image file. This storage will be enumerated to place all substorages and streams in the root file system of the stage image file. Substorages become folders and streams become files. Multiple calls to this method can be repeated to slowly stage an image file without wasting undue amounts of hard drive space building up a storage file.


## -parameters




### -param pStorage [in]

Path to the storage whose subitems are to be added to the root of the staged image file.


### -param lFileOverwrite [in]

If this parameter is nonzero, overwrite existing files with the same name. Otherwise, the last file added appears in the directory.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



When you repeat an 
<b>AddData</b> operation, folders with duplicate files cause a test of  <i>lFileOverwrite</i>. If the flag is nonzero, the file is overwritten. Earlier files with conflicting names are still written to disc from the image file. If <i>lFileOverwrite</i> is zero and a file with the same name exists, 
<b>AddData</b> fails with IMAPI_E_FILEEXISTS.

While 
<b>AddData</b> can be called multiple times after calling 
<a href="https://msdn.microsoft.com/5f2e9135-d251-4702-b5d1-51d9b445a4f5">IDiscMaster::SetActiveDiscRecorder</a>, 
<b>SetActiveDiscRecorder</b> must be called any time a new image is started, and immediately before the first 
<b>AddData</b> call, regardless of whether the burner is the same one used in the previous image creation.

If a call to this method would overrun the number of available data blocks, the method returns IMAPI_E_DISCFULL and ignores all data that was to be added. This ensures that the final Joliet file system is not corrupted.




## -see-also




<a href="https://msdn.microsoft.com/e2269b68-1860-4afd-90f2-d61297f3fa9b">IJolietDiscMaster</a>
 

 

