---
UID: NF:shobjidl.IQueryCancelAutoPlay.AllowAutoPlay
title: IQueryCancelAutoPlay::AllowAutoPlay (shobjidl.h)
description: Determines whether to play media inserted by a user and if so using what restrictions.
helpviewer_keywords: ["ARCONTENT_AUDIOCD","ARCONTENT_AUTOPLAYMUSIC","ARCONTENT_AUTOPLAYPIX","ARCONTENT_AUTOPLAYVIDEO","ARCONTENT_AUTORUNINF","ARCONTENT_BLANKBD","ARCONTENT_BLANKCD","ARCONTENT_BLANKDVD","ARCONTENT_BLURAY","ARCONTENT_CAMERASTORAGE","ARCONTENT_CUSTOMEVENT","ARCONTENT_DVDAUDIO","ARCONTENT_DVDMOVIE","ARCONTENT_MASK","ARCONTENT_NONE","ARCONTENT_PHASE_FINAL","ARCONTENT_PHASE_MASK","ARCONTENT_PHASE_PRESNIFF","ARCONTENT_PHASE_SNIFFING","ARCONTENT_PHASE_UNKNOWN","ARCONTENT_SVCD","ARCONTENT_UNKNOWNCONTENT","ARCONTENT_VCD","AllowAutoPlay","AllowAutoPlay method [Windows Shell]","AllowAutoPlay method [Windows Shell]","IQueryCancelAutoPlay interface","IQueryCancelAutoPlay interface [Windows Shell]","AllowAutoPlay method","IQueryCancelAutoPlay.AllowAutoPlay","IQueryCancelAutoPlay::AllowAutoPlay","_shell_IQueryCancelAutoPlay_AllowAutoPlay","shell.IQueryCancelAutoPlay_AllowAutoPlay","shobjidl/IQueryCancelAutoPlay::AllowAutoPlay"]
old-location: shell\IQueryCancelAutoPlay_AllowAutoPlay.htm
tech.root: shell
ms.assetid: ebc826a2-d7ea-413a-836b-c7e51f13692a
ms.date: 12/05/2018
ms.keywords: ARCONTENT_AUDIOCD, ARCONTENT_AUTOPLAYMUSIC, ARCONTENT_AUTOPLAYPIX, ARCONTENT_AUTOPLAYVIDEO, ARCONTENT_AUTORUNINF, ARCONTENT_BLANKBD, ARCONTENT_BLANKCD, ARCONTENT_BLANKDVD, ARCONTENT_BLURAY, ARCONTENT_CAMERASTORAGE, ARCONTENT_CUSTOMEVENT, ARCONTENT_DVDAUDIO, ARCONTENT_DVDMOVIE, ARCONTENT_MASK, ARCONTENT_NONE, ARCONTENT_PHASE_FINAL, ARCONTENT_PHASE_MASK, ARCONTENT_PHASE_PRESNIFF, ARCONTENT_PHASE_SNIFFING, ARCONTENT_PHASE_UNKNOWN, ARCONTENT_SVCD, ARCONTENT_UNKNOWNCONTENT, ARCONTENT_VCD, AllowAutoPlay, AllowAutoPlay method [Windows Shell], AllowAutoPlay method [Windows Shell],IQueryCancelAutoPlay interface, IQueryCancelAutoPlay interface [Windows Shell],AllowAutoPlay method, IQueryCancelAutoPlay.AllowAutoPlay, IQueryCancelAutoPlay::AllowAutoPlay, _shell_IQueryCancelAutoPlay_AllowAutoPlay, shell.IQueryCancelAutoPlay_AllowAutoPlay, shobjidl/IQueryCancelAutoPlay::AllowAutoPlay
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryCancelAutoPlay::AllowAutoPlay
 - shobjidl/IQueryCancelAutoPlay::AllowAutoPlay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryCancelAutoPlay.AllowAutoPlay
---

# IQueryCancelAutoPlay::AllowAutoPlay


## -description

Determines whether to play media inserted by a user and if so using what restrictions.

## -parameters

### -param pszPath [in]

Type: <b>LPCWSTR</b>

The drive letter in the form <b>D:\\</b>

### -param dwContentType [in]

Type: <b>DWORD</b>

The type of content as specified by the following flags.



#### ARCONTENT_AUTORUNINF (0x00000002)

Use the Autorun.inf file. This is the traditional AutoRun behavior.



#### ARCONTENT_AUDIOCD (0x00000004)

AutoRun audio CDs.



#### ARCONTENT_DVDMOVIE (0x00000008)

AutoRun DVDs.



#### ARCONTENT_BLANKCD (0x00000010)

AutoPlay blank CD-Rs and CD-RWs.



#### ARCONTENT_BLANKDVD (0x00000020)

AutoPlay blank DVD-Rs and DVD-RAMs.



#### ARCONTENT_UNKNOWNCONTENT (0x00000040)

AutoRun if the media is formatted and the content does not fall under a type covered by one of the other flags.



#### ARCONTENT_AUTOPLAYPIX (0x00000080)

AutoPlay if the content consists of file types defined as pictures, such as .bmp and .jpg files.



#### ARCONTENT_AUTOPLAYMUSIC (0x00000100)

AutoPlay if the content consists of file types defined as music, such as MP3 files.



#### ARCONTENT_AUTOPLAYVIDEO (0x00000200)

AutoPlay if the content consists of file types defined as video files.



#### ARCONTENT_VCD (0x00000400)

<b>Introduced in Windows Vista</b>. AutoPlay video CDs (VCDs).



#### ARCONTENT_SVCD (0x00000800)

<b>Introduced in Windows Vista</b>. AutoPlay Super Video CD (SVCD) media.



#### ARCONTENT_DVDAUDIO (0x00001000)

<b>Introduced in Windows Vista</b>. AutoPlay DVD-Audio media.



#### ARCONTENT_BLANKBD (0x00002000)

AutoPlay blank recordable high definition DVD media in the Blu-ray Disc™ format (BD-R or BD-RW). Note: Prior to Windows 7, this value was defined to specify non-recordable media in the HD DVD format.



#### ARCONTENT_BLURAY (0x00004000)

<b>Introduced in Windows Vista</b>. AutoPlay high definition DVD media in the Blu-ray Disc™ format.



#### ARCONTENT_CAMERASTORAGE (0x00008000)

<b>Introduced in Windows 8</b>.



#### ARCONTENT_CUSTOMEVENT (0x00010000)

<b>Introduced in Windows 8</b>.



#### ARCONTENT_NONE (0x00000000)

<b>Introduced in Windows Vista</b>. AutoPlay empty but formatted media.



#### ARCONTENT_MASK (0x0001FFFE)

<b>Introduced in Windows Vista</b>. A mask that denotes valid ARCONTENT flag values for media types. This mask does not include ARCONTENT_PHASE values.



#### ARCONTENT_PHASE_UNKNOWN (0x00000000)

<b>Introduced in Windows Vista</b>. AutoPlay is searching the media. The phase of the search (presniff, sniffing, or final) is unknown.



#### ARCONTENT_PHASE_PRESNIFF (0x10000000)

<b>Introduced in Windows Vista</b>. The contents of the media are known before the media is searched, due to the media type; for instance, audio CDs and DVD movies.



#### ARCONTENT_PHASE_SNIFFING (0x20000000)

<b>Introduced in Windows Vista</b>. AutoPlay is currently searching the media. Any results reported during this phase should be considered a partial list as more content types might still be found.



#### ARCONTENT_PHASE_FINAL (0x40000000)

<b>Introduced in Windows Vista</b>. AutoPlay has finished searching the media. Results reported are final.



#### ARCONTENT_PHASE_MASK (0x70000000)

<b>Introduced in Windows Vista</b>. A mask that denotes valid ARCONTENT_PHASE values.

### -param pszLabel [in]

Type: <b>LPCWSTR</b>

The media label.

### -param dwSerialNumber [in]

Type: <b>DWORD</b>

The media serial number.

## -returns

Type: <b>HRESULT</b>

Returns S_OK to allow AutoRun or S_FALSE to cancel AutoRun.

## -remarks

Applications register an instance of the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-iquerycancelautoplay">IQueryCancelAutoPlay</a> interface in the running object table (ROT). Before the Shell starts AutoRun or AutoPlay, when the user inserts new media, it checks the ROT for a component implementing <b>IQueryCancelAutoPlay</b>. If it finds one, the Shell calls that implementation's <b>IQueryCancelAutoPlay::AllowAutoPlay</b> method to determine whether it should proceed, and using what restrictions.

Upon presentation of media, the Shell searches the ROT for a component implementing <a href="/windows/desktop/api/shobjidl/nn-shobjidl-iquerycancelautoplay">IQueryCancelAutoPlay</a>. If one is found, the class identifier (CLSID) of that component's moniker is extracted. The presence of a ROT registration informs the Shell that the component might want to cancel AutoRun or AutoPlay. For confirmation, the Shell must also find a registry key for that same CLSID at the following location:

<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>Current Version</b>
               <b>Explorer</b>
                  <b>AutoplayHandlers</b>
                     <b>CancelAutoplay</b>
                        <b>CLSID</b>
                           <i>The component's CLSID</i></pre>This value is added by the application or hardware, usually at installation time. It isn't assigned a data value.

<div class="alert"><b>Note</b>  The CLSID entered as a value under this key should not be encased in curly brackets.</div>
<div> </div>
