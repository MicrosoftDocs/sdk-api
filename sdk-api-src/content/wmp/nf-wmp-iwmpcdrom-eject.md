---
UID: NF:wmp.IWMPCdrom.eject
title: IWMPCdrom::eject (wmp.h)
description: The eject method ejects the CD or DVD from the drive.
helpviewer_keywords: ["IWMPCdrom interface [Windows Media Player]","eject method","IWMPCdrom.eject","IWMPCdrom::eject","IWMPCdromeject","eject","eject method [Windows Media Player]","eject method [Windows Media Player]","IWMPCdrom interface","wmp.iwmpcdrom_eject","wmp/IWMPCdrom::eject"]
old-location: wmp\iwmpcdrom_eject.htm
tech.root: WMP
ms.assetid: 1b17c405-0887-4948-b375-c1ebcf2a72b3
ms.date: 12/05/2018
ms.keywords: IWMPCdrom interface [Windows Media Player],eject method, IWMPCdrom.eject, IWMPCdrom::eject, IWMPCdromeject, eject, eject method [Windows Media Player], eject method [Windows Media Player],IWMPCdrom interface, wmp.iwmpcdrom_eject, wmp/IWMPCdrom::eject
f1_keywords:
- wmp/IWMPCdrom.eject
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
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
- IWMPCdrom.eject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCdrom::eject


## -description



The <b>eject</b> method ejects the CD or DVD from the drive.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If the drive door is open, this method closes the door.

To use this method, read access to the library is required. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcdrom">IWMPCdromInterface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_playstate">IWMPCore::get_playState</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-requestmediaaccessrights">IWMPSettings2::requestMediaAccessRights</a>
 

 

