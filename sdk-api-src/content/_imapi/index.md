---
UID: TP:imapi
ms.assetid: d5ee2b29-ba7f-3360-9fd6-16f32572a676
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Image Mastering API



Overview of the Image Mastering API technology.

To develop Image Mastering API, you need these headers:

 * [imapi.h](..\imapi\index.md)
 * [imapi2.h](..\imapi2\index.md)
 * [imapi2fs.h](..\imapi2fs\index.md)

For the programming guide, see [Image Mastering API](/windows/desktop/imapi).

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [EmulationType enumeration](..\imapi2fs\ne-imapi2fs-emulationtype.md) | Defines values for media types that the boot image is intended to emulate. |
| [FsiFileSystems enumeration](..\imapi2fs\ne-imapi2fs-fsifilesystems.md) | Defines values for recognized file systems. |
| [FsiItemType enumeration](..\imapi2fs\ne-imapi2fs-fsiitemtype.md) | Defines values for the file system item that was found using the IFileSystemImage |
| [PlatformId enumeration](..\imapi2fs\ne-imapi2fs-platformid.md) | Defines values for the operating system architecture that the boot image supports. |
| [_IMAPI_BURN_VERIFICATION_LEVEL enumeration](..\imapi2\ne-imapi2-_imapi_burn_verification_level.md) | Defines values for the burn verification implemented by the IBurnVerification interface. |
| [_IMAPI_CD_SECTOR_TYPE enumeration](..\imapi2\ne-imapi2-_imapi_cd_sector_type.md) | Defines the sector types that can be written to CD media. |
| [_IMAPI_CD_TRACK_DIGITAL_COPY_SETTING enumeration](..\imapi2\ne-imapi2-_imapi_cd_track_digital_copy_setting.md) | Defines the digital copy setting values available for a given track. |
| [_IMAPI_FEATURE_PAGE_TYPE enumeration](..\imapi2\ne-imapi2-_imapi_feature_page_type.md) | Defines values for the feature that are supported by the logical unit (CD and DVD device). |
| [_IMAPI_FORMAT2_DATA_MEDIA_STATE enumeration](..\imapi2\ne-imapi2-_imapi_format2_data_media_state.md) | Defines values for the possible media states. |
| [_IMAPI_FORMAT2_DATA_WRITE_ACTION enumeration](..\imapi2\ne-imapi2-_imapi_format2_data_write_action.md) | Defines values that indicate the current state of the write operation when using the IDiscFormat2DataEventArgs interface. |
| [_IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE enumeration](..\imapi2\ne-imapi2-_imapi_format2_raw_cd_data_sector_type.md) | Defines values that indicate the type of sub-channel data. |
| [_IMAPI_FORMAT2_RAW_CD_WRITE_ACTION enumeration](..\imapi2\ne-imapi2-_imapi_format2_raw_cd_write_action.md) | Defines values that indicate the current state of the write operation when using the IDiscFormat2RawCDEventArgs interface. |
| [_IMAPI_FORMAT2_TAO_WRITE_ACTION enumeration](..\imapi2\ne-imapi2-_imapi_format2_tao_write_action.md) | Defines values that indicate the current state of the write operation when using the IDiscFormat2TrackAtOnceEventArgs interface. |
| [_IMAPI_MEDIA_PHYSICAL_TYPE enumeration](..\imapi2\ne-imapi2-_imapi_media_physical_type.md) | Defines values for the currently known media types supported by IMAPI. |
| [_IMAPI_MEDIA_WRITE_PROTECT_STATE enumeration](..\imapi2\ne-imapi2-_imapi_media_write_protect_state.md) | Defines values that indicate the media write protect status. One or more write protect values can be set on a given drive. |
| [_IMAPI_MODE_PAGE_REQUEST_TYPE enumeration](..\imapi2\ne-imapi2-_imapi_mode_page_request_type.md) | Defines values that indicate requests sent to a device using the MODE_SENSE10 MMC command. |
| [_IMAPI_MODE_PAGE_TYPE enumeration](..\imapi2\ne-imapi2-_imapi_mode_page_type.md) | Defines values for the mode pages that are supported by CD and DVD devices. |
| [_IMAPI_PROFILE_TYPE enumeration](..\imapi2\ne-imapi2-_imapi_profile_type.md) | Defines values for the possible profiles of a CD and DVD device. A profile defines the type of media and features that the device supports. |
| [_IMAPI_READ_TRACK_ADDRESS_TYPE enumeration](..\imapi2\ne-imapi2-_imapi_read_track_address_type.md) | Defines values that indicate how to interpret track addresses for the current disc profile of a randomly-writable, hardware-defect-managed media type. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [DDiscFormat2DataEvents interface](..\imapi2\nn-imapi2-ddiscformat2dataevents.md) | Implement this interface to receive notifications of the current write operation. |
| [DDiscFormat2EraseEvents interface](..\imapi2\nn-imapi2-ddiscformat2eraseevents.md) | Implement this interface to receive notifications of the current erase operation. |
| [DDiscFormat2RawCDEvents interface](..\imapi2\nn-imapi2-ddiscformat2rawcdevents.md) | Implement this interface to receive notifications of the current raw-image write operation. |
| [DDiscFormat2TrackAtOnceEvents interface](..\imapi2\nn-imapi2-ddiscformat2trackatonceevents.md) | Implement this interface to receive notifications of the current track-writing operation. |
| [DDiscMaster2Events interface](..\imapi2\nn-imapi2-ddiscmaster2events.md) | Implement this interface to receive notification when a CD or DVD device is added to or removed from the computer. |
| [DFileSystemImageEvents interface](..\imapi2fs\nn-imapi2fs-dfilesystemimageevents.md) | Implement this interface to receive notifications of the current write operation. |
| [DFileSystemImageImportEvents interface](..\imapi2fs\nn-imapi2fs-dfilesystemimageimportevents.md) | Use this interface to receives notifications regarding the current file system import operation. |
| [DWriteEngine2Events interface](..\imapi2\nn-imapi2-dwriteengine2events.md) | Implement this interface to receive notifications of the current write operation. |
| [IBlockRange interface](..\imapi2\nn-imapi2-iblockrange.md) | Use this interface to retrieve information about a single continuous range of sectors on the media. This interface is typically used together with the IBlockRangeList interface to describe a collection of sector ranges. |
| [IBlockRangeList interface](..\imapi2\nn-imapi2-iblockrangelist.md) | Use this interface to retrieve a list of continuous sector ranges on the media. This interface is used to describe the sectors that need to be updated on a rewritable disc when a new logical session is recorded. |
| [IBootOptions interface](..\imapi2fs\nn-imapi2fs-ibootoptions.md) | Use this interface to specify the boot image to add to the optical disc. A boot image contains one or more sectors of code used to start the computer. |
| [IBurnVerification interface](..\imapi2\nn-imapi2-iburnverification.md) | Use this interface with IDiscFormat2Data or IDiscFormat2TrackAtOnce to get or set the Burn Verification Level property which dictates how burned media is verified for integrity after the write operation. |
| [IDiscFormat2 interface](..\imapi2\nn-imapi2-idiscformat2.md) | This is a base interface. Use the following interfaces which inherit this interface |
| [IDiscFormat2Data interface](..\imapi2\nn-imapi2-idiscformat2data.md) | Use this interface to write a data stream to a disc. |
| [IDiscFormat2DataEventArgs interface](..\imapi2\nn-imapi2-idiscformat2dataeventargs.md) | Use this interface to retrieve information about the current write operation. |
| [IDiscFormat2Erase interface](..\imapi2\nn-imapi2-idiscformat2erase.md) | Use this interface to erase data from a disc. |
| [IDiscFormat2RawCD interface](..\imapi2\nn-imapi2-idiscformat2rawcd.md) | Use this interface to write raw images to a disc device using Disc At Once (DAO) mode (also known as uninterrupted recording). |
| [IDiscFormat2RawCDEventArgs interface](..\imapi2\nn-imapi2-idiscformat2rawcdeventargs.md) | Use this interface to retrieve information about the current write operation. |
| [IDiscFormat2TrackAtOnce interface](..\imapi2\nn-imapi2-idiscformat2trackatonce.md) | Use this interface to write audio to blank CD-R or CD-RW media in Track-At-Once mode. |
| [IDiscFormat2TrackAtOnceEventArgs interface](..\imapi2\nn-imapi2-idiscformat2trackatonceeventargs.md) | Use this interface to retrieve information about the current write operation. |
| [IDiscMaster interface](..\imapi\nn-imapi-idiscmaster.md) | The IDiscMaster interface allows an application to reserve an image mastering API, enumerate disc mastering formats and disc recorders supported by an image mastering object, and start a simulated or actual burn of a disc. |
| [IDiscMaster2 interface](..\imapi2\nn-imapi2-idiscmaster2.md) | Use this interface to enumerate the CD and DVD devices installed on the computer. |
| [IDiscMasterProgressEvents interface](..\imapi\nn-imapi-idiscmasterprogressevents.md) | The IDiscMasterProgressEvents interface provides a single interface for all callbacks that can be made from IMAPI to an application. |
| [IDiscRecorder interface](..\imapi\nn-imapi-idiscrecorder.md) | The IDiscRecorder interface enables access to a single disc recorder device, labeled the active disc recorder. An IMAPI object such as MSDiscMasterObj maintains an active disc recorder. |
| [IDiscRecorder2 interface](..\imapi2\nn-imapi2-idiscrecorder2.md) | This interface represents a physical device. You use this interface to retrieve information about a CD and DVD device installed on the computer and to perform operations such as closing the tray or eject the media. |
| [IDiscRecorder2Ex interface](..\imapi2\nn-imapi2-idiscrecorder2ex.md) | This interface represents a physical device. |
| [IEnumFsiItems interface](..\imapi2fs\nn-imapi2fs-ienumfsiitems.md) | Use this interface to enumerate the child directory and file items for a FsiDirectoryItem object. |
| [IEnumProgressItems interface](..\imapi2fs\nn-imapi2fs-ienumprogressitems.md) | Use this interface to enumerate a collection of progress items. |
| [IFileSystemImage interface](..\imapi2fs\nn-imapi2fs-ifilesystemimage.md) | Use this interface to build a file system image, set session parameter, and import or export an image. |
| [IFileSystemImage2 interface](..\imapi2fs\nn-imapi2fs-ifilesystemimage2.md) | Use this interface to write multiple boot entries or boot images required for the EFI/UEFI support. For example, boot media with boot straps for both Windows XP and Windows Vista. |
| [IFileSystemImage3 interface](..\imapi2fs\nn-imapi2fs-ifilesystemimage3.md) | Use this interface to set or check the metadata and metadata mirror files in a UDF file system (rev 2.50 and later) to determine redundancy. |
| [IFileSystemImageResult interface](..\imapi2fs\nn-imapi2fs-ifilesystemimageresult.md) | Use this interface to get information about the burn image, the image data stream, and progress information. |
| [IFileSystemImageResult2 interface](..\imapi2fs\nn-imapi2fs-ifilesystemimageresult2.md) | The IFileSystemImageResult2 interface allows the data recorder object to retrieve information about modified blocks in images created for rewritable discs. |
| [IFsiDirectoryItem interface](..\imapi2fs\nn-imapi2fs-ifsidirectoryitem.md) | Use this interface to add items to or remove items from the file-system image. |
| [IFsiDirectoryItem2 interface](..\imapi2fs\nn-imapi2fs-ifsidirectoryitem2.md) | Use this interface to add a directory tree, which includes all sub-directories, files, and associated named streams to a file system image. |
| [IFsiFileItem interface](..\imapi2fs\nn-imapi2fs-ifsifileitem.md) | Use this interface to identify the file size and data stream of the file contents. |
| [IFsiFileItem2 interface](..\imapi2fs\nn-imapi2fs-ifsifileitem2.md) | Use this interface to add, remove and enumerate named streams associated with a file. This interface also provides access to the 'Real-Time' attribute of a file. |
| [IFsiItem interface](..\imapi2fs\nn-imapi2fs-ifsiitem.md) | Base interface containing properties common to both file and directory items. |
| [IFsiNamedStreams interface](..\imapi2fs\nn-imapi2fs-ifsinamedstreams.md) | Use this interface to enumerate the named streams associated with a file in a file system image. |
| [IIsoImageManager interface](..\imapi2fs\nn-imapi2fs-iisoimagemanager.md) | Use this interface to verify if an existing .iso file contains a valid file system for burning. |
| [IJolietDiscMaster interface](..\imapi\nn-imapi-ijolietdiscmaster.md) | The IJolietDiscMaster interface enables the staging of a CD data disc. |
| [IMultisession interface](..\imapi2\nn-imapi2-imultisession.md) | Base interface containing properties common to derived multisession interfaces. |
| [IMultisessionRandomWrite interface](..\imapi2\nn-imapi2-imultisessionrandomwrite.md) | Use this interface to retrieve information about the current state of media allowing random writes and not supporting the concept of physical sessions. |
| [IMultisessionSequential interface](..\imapi2\nn-imapi2-imultisessionsequential.md) | Use this interface to retrieve information about the previous import session on a sequentially recorded media, if the media contains a previous session. |
| [IMultisessionSequential2 interface](..\imapi2\nn-imapi2-imultisessionsequential2.md) | Use this interface to retrieve information about the size of a writeable unit on sequentially recorded media. |
| [IProgressItem interface](..\imapi2fs\nn-imapi2fs-iprogressitem.md) | Use this interface to retrieve block information for one segment of the result file image. |
| [IProgressItems interface](..\imapi2fs\nn-imapi2fs-iprogressitems.md) | Use this interface to enumerate the progress items in a result image. |
| [IRawCDImageCreator interface](..\imapi2\nn-imapi2-irawcdimagecreator.md) | Use this interface to create a RAW CD image for use in writing to CD media in Disc-at-Once (DAO) mode. Images created with this interface can be written to CD media using the IDiscFormat2RawCD interface. |
| [IRawCDImageTrackInfo interface](..\imapi2\nn-imapi2-irawcdimagetrackinfo.md) | Use this interface to track per-track properties that are applied to CD media. |
| [IRedbookDiscMaster interface](..\imapi\nn-imapi-iredbookdiscmaster.md) | The IRedbookDiscMaster interface enables the staging of an audio CD image. It represents one of the formats supported by MSDiscMasterObj, and it allows the creation of multi-track audio discs in Track-at-Once mode (fixed-size audio gaps). |
| [IStreamConcatenate interface](..\imapi2\nn-imapi2-istreamconcatenate.md) | Use this interface to combine several data streams into a single stream. |
| [IStreamInterleave interface](..\imapi2\nn-imapi2-istreaminterleave.md) | Use this interface to combine several data streams into a single stream by alternately interspersing portions of each. |
| [IStreamPseudoRandomBased interface](..\imapi2\nn-imapi2-istreampseudorandombased.md) | Use this interface to generate a read-only data stream whose data is initialized with pseudo-random data (not cryptographically safe). You must call the SetSize method to set the requested size of the stream. |
| [IWriteEngine2 interface](..\imapi2\nn-imapi2-iwriteengine2.md) | Use this interface to write a data stream to a device. |
| [IWriteEngine2EventArgs interface](..\imapi2\nn-imapi2-iwriteengine2eventargs.md) | Use this interface to retrieve information about the current write operation. This interface is passed to the DWriteEngine2Events |
| [IWriteSpeedDescriptor interface](..\imapi2\nn-imapi2-iwritespeeddescriptor.md) | Use this interface retrieve detailed write configurations supported by the disc recorder and current media, for example, the media type, write speed, rotational-speed control type. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [DDiscFormat2DataEvents::Update](..\imapi2\nf-imapi2-ddiscformat2dataevents-update.md) | Implement this method to receive progress notification of the current write operation. |
| [DDiscFormat2EraseEvents::Update](..\imapi2\nf-imapi2-ddiscformat2eraseevents-update.md) | Implement this method to receive progress notification of the current erase operation. |
| [DDiscFormat2RawCDEvents::Update](..\imapi2\nf-imapi2-ddiscformat2rawcdevents-update.md) | Implement this method to receive progress notification of the current raw-image write operation. |
| [DDiscFormat2TrackAtOnceEvents::Update](..\imapi2\nf-imapi2-ddiscformat2trackatonceevents-update.md) | Implement this method to receive progress notification of the current track-writing operation. |
| [DDiscMaster2Events::NotifyDeviceAdded](..\imapi2\nf-imapi2-ddiscmaster2events-notifydeviceadded.md) | Receives notification when an optical media device is added to the computer. |
| [DDiscMaster2Events::NotifyDeviceRemoved](..\imapi2\nf-imapi2-ddiscmaster2events-notifydeviceremoved.md) | Receives notification when an optical media device is removed from the computer. |
| [DFileSystemImageEvents::Update](..\imapi2fs\nf-imapi2fs-dfilesystemimageevents-update.md) | Implement this method to receive progress notification of the current write operation. The notifications are sent when copying the content of a file or while adding directories or files to the file system image. |
| [DFileSystemImageImportEvents::UpdateImport](..\imapi2fs\nf-imapi2fs-dfilesystemimageimportevents-updateimport.md) | Receives import notification for every file and directory item imported from an optical medium. |
| [DWriteEngine2Events::Update](..\imapi2\nf-imapi2-dwriteengine2events-update.md) | Implement this method to receive progress notification of the current write operation. |
| [IBlockRange::get_EndLba](..\imapi2\nf-imapi2-iblockrange-get_endlba.md) | Retrieves the end sector of the range specified by the IBlockRange interface. |
| [IBlockRange::get_StartLba](..\imapi2\nf-imapi2-iblockrange-get_startlba.md) | Retrieves the start sector of the range described by IBlockRange. |
| [IBlockRangeList::get_BlockRanges](..\imapi2\nf-imapi2-iblockrangelist-get_blockranges.md) | Returns the list of sector ranges in the form of a safe array of variants of type VT_Dispatch. |
| [IBootOptions::AssignBootImage](..\imapi2fs\nf-imapi2fs-ibootoptions-assignbootimage.md) | Sets the data stream that contains the boot image. |
| [IBootOptions::get_BootImage](..\imapi2fs\nf-imapi2fs-ibootoptions-get_bootimage.md) | Retrieves a pointer to the boot image data stream. |
| [IBootOptions::get_Emulation](..\imapi2fs\nf-imapi2fs-ibootoptions-get_emulation.md) | Retrieves the media type that the boot image is intended to emulate. |
| [IBootOptions::get_ImageSize](..\imapi2fs\nf-imapi2fs-ibootoptions-get_imagesize.md) | Retrieves the size of the boot image. |
| [IBootOptions::get_Manufacturer](..\imapi2fs\nf-imapi2fs-ibootoptions-get_manufacturer.md) | Retrieves the identifier of the manufacturer of the CD. |
| [IBootOptions::get_PlatformId](..\imapi2fs\nf-imapi2fs-ibootoptions-get_platformid.md) | Retrieves the platform identifier that identifies the operating system architecture that the boot image supports. |
| [IBootOptions::put_Emulation](..\imapi2fs\nf-imapi2fs-ibootoptions-put_emulation.md) | Sets the media type that the boot image is intended to emulate. |
| [IBootOptions::put_Manufacturer](..\imapi2fs\nf-imapi2fs-ibootoptions-put_manufacturer.md) | Sets an identifier that identifies the manufacturer or developer of the CD. |
| [IBootOptions::put_PlatformId](..\imapi2fs\nf-imapi2fs-ibootoptions-put_platformid.md) | Sets the platform identifier that identifies the operating system architecture that the boot image supports. |
| [IBurnVerification::get_BurnVerificationLevel](..\imapi2\nf-imapi2-iburnverification-get_burnverificationlevel.md) | Retrieves the current Burn Verification Level. |
| [IBurnVerification::put_BurnVerificationLevel](..\imapi2\nf-imapi2-iburnverification-put_burnverificationlevel.md) | Sets the Burn Verification Level. |
| [IDiscFormat2::IsCurrentMediaSupported](..\imapi2\nf-imapi2-idiscformat2-iscurrentmediasupported.md) | Determines if the current media in a supported recorder supports the given format. |
| [IDiscFormat2::IsRecorderSupported](..\imapi2\nf-imapi2-idiscformat2-isrecordersupported.md) | Determines if the recorder supports the given format. |
| [IDiscFormat2::get_MediaHeuristicallyBlank](..\imapi2\nf-imapi2-idiscformat2-get_mediaheuristicallyblank.md) | Attempts to determine if the media is blank using heuristics (mainly for DVD+RW and DVD-RAM media). |
| [IDiscFormat2::get_MediaPhysicallyBlank](..\imapi2\nf-imapi2-idiscformat2-get_mediaphysicallyblank.md) | Determines if the current media is reported as physically blank by the drive. |
| [IDiscFormat2::get_SupportedMediaTypes](..\imapi2\nf-imapi2-idiscformat2-get_supportedmediatypes.md) | Retrieves the media types that are supported by the current implementation of the IDiscFormat2 interface. |
| [IDiscFormat2Data::CancelWrite](..\imapi2\nf-imapi2-idiscformat2data-cancelwrite.md) | Cancels the current write operation. |
| [IDiscFormat2Data::SetWriteSpeed](..\imapi2\nf-imapi2-idiscformat2data-setwritespeed.md) | Sets the write speed of the disc recorder. |
| [IDiscFormat2Data::Write](..\imapi2\nf-imapi2-idiscformat2data-write.md) | Writes the data stream to the device. |
| [IDiscFormat2Data::get_BufferUnderrunFreeDisabled](..\imapi2\nf-imapi2-idiscformat2data-get_bufferunderrunfreedisabled.md) | Determines if Buffer Underrun Free recording is enabled for CDR, CD-RW, and DVD-R media. |
| [IDiscFormat2Data::get_ClientName](..\imapi2\nf-imapi2-idiscformat2data-get_clientname.md) | Retrieves the friendly name of the client. |
| [IDiscFormat2Data::get_CurrentMediaStatus](..\imapi2\nf-imapi2-idiscformat2data-get_currentmediastatus.md) | Retrieves the current state of the media in the device. |
| [IDiscFormat2Data::get_CurrentPhysicalMediaType](..\imapi2\nf-imapi2-idiscformat2data-get_currentphysicalmediatype.md) | Retrieves the type of media in the disc device. |
| [IDiscFormat2Data::get_CurrentRotationTypeIsPureCAV](..\imapi2\nf-imapi2-idiscformat2data-get_currentrotationtypeispurecav.md) | Retrieves the current rotational-speed control used by the recorder. |
| [IDiscFormat2Data::get_CurrentWriteSpeed](..\imapi2\nf-imapi2-idiscformat2data-get_currentwritespeed.md) | Retrieves the drive's current write speed. |
| [IDiscFormat2Data::get_DisableConsumerDvdCompatibilityMode](..\imapi2\nf-imapi2-idiscformat2data-get_disableconsumerdvdcompatibilitymode.md) | Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD. |
| [IDiscFormat2Data::get_ForceMediaToBeClosed](..\imapi2\nf-imapi2-idiscformat2data-get_forcemediatobeclosed.md) | Determines if further additions to the file system are prevented. |
| [IDiscFormat2Data::get_ForceOverwrite](..\imapi2\nf-imapi2-idiscformat2data-get_forceoverwrite.md) | Determines if the data writer must overwrite the disc on overwritable media types. |
| [IDiscFormat2Data::get_FreeSectorsOnMedia](..\imapi2\nf-imapi2-idiscformat2data-get_freesectorsonmedia.md) | Retrieves the number of free sectors on the disc for incremental recording (without overwriting existing data). |
| [IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession](..\imapi2\nf-imapi2-idiscformat2data-get_lastwrittenaddressofprevioussession.md) | Retrieves the last sector of the previous write session. |
| [IDiscFormat2Data::get_MultisessionInterfaces](..\imapi2\nf-imapi2-idiscformat2data-get_multisessioninterfaces.md) | Retrieves a list of available multi-session interfaces. |
| [IDiscFormat2Data::get_NextWritableAddress](..\imapi2\nf-imapi2-idiscformat2data-get_nextwritableaddress.md) | Retrieves the location for the next write operation. |
| [IDiscFormat2Data::get_PostgapAlreadyInImage](..\imapi2\nf-imapi2-idiscformat2data-get_postgapalreadyinimage.md) | Determines if the data stream contains post-writing gaps. |
| [IDiscFormat2Data::get_Recorder](..\imapi2\nf-imapi2-idiscformat2data-get_recorder.md) | Retrieves the recording device to use for the write operation. |
| [IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV](..\imapi2\nf-imapi2-idiscformat2data-get_requestedrotationtypeispurecav.md) | Retrieves the requested rotational-speed control type. |
| [IDiscFormat2Data::get_RequestedWriteSpeed](..\imapi2\nf-imapi2-idiscformat2data-get_requestedwritespeed.md) | Retrieves the requested write speed. |
| [IDiscFormat2Data::get_StartAddressOfPreviousSession](..\imapi2\nf-imapi2-idiscformat2data-get_startaddressofprevioussession.md) | Retrieves the first sector of the previous write session. |
| [IDiscFormat2Data::get_SupportedWriteSpeedDescriptors](..\imapi2\nf-imapi2-idiscformat2data-get_supportedwritespeeddescriptors.md) | Retrieves a list of the detailed write configurations supported by the disc recorder and current media. |
| [IDiscFormat2Data::get_SupportedWriteSpeeds](..\imapi2\nf-imapi2-idiscformat2data-get_supportedwritespeeds.md) | Retrieves a list of the write speeds supported by the disc recorder and current media. |
| [IDiscFormat2Data::get_TotalSectorsOnMedia](..\imapi2\nf-imapi2-idiscformat2data-get_totalsectorsonmedia.md) | Retrieves the number of sectors on the media in the device. |
| [IDiscFormat2Data::get_WriteProtectStatus](..\imapi2\nf-imapi2-idiscformat2data-get_writeprotectstatus.md) | Retrieves the current write protect state of the media in the device. |
| [IDiscFormat2Data::put_BufferUnderrunFreeDisabled](..\imapi2\nf-imapi2-idiscformat2data-put_bufferunderrunfreedisabled.md) | Determines if Buffer Underrun Free recording is enabled. |
| [IDiscFormat2Data::put_ClientName](..\imapi2\nf-imapi2-idiscformat2data-put_clientname.md) | Sets the friendly name of the client. |
| [IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode](..\imapi2\nf-imapi2-idiscformat2data-put_disableconsumerdvdcompatibilitymode.md) | Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD. |
| [IDiscFormat2Data::put_ForceMediaToBeClosed](..\imapi2\nf-imapi2-idiscformat2data-put_forcemediatobeclosed.md) | Determines if further additions to the file system are prevented. |
| [IDiscFormat2Data::put_ForceOverwrite](..\imapi2\nf-imapi2-idiscformat2data-put_forceoverwrite.md) | Determines if the data writer must overwrite the disc on overwritable media types. |
| [IDiscFormat2Data::put_PostgapAlreadyInImage](..\imapi2\nf-imapi2-idiscformat2data-put_postgapalreadyinimage.md) | Determines if the data stream contains post-writing gaps. |
| [IDiscFormat2Data::put_Recorder](..\imapi2\nf-imapi2-idiscformat2data-put_recorder.md) | Sets the recording device to use for the write operation. |
| [IDiscFormat2DataEventArgs::get_CurrentAction](..\imapi2\nf-imapi2-idiscformat2dataeventargs-get_currentaction.md) | Retrieves the current write action being performed. |
| [IDiscFormat2DataEventArgs::get_ElapsedTime](..\imapi2\nf-imapi2-idiscformat2dataeventargs-get_elapsedtime.md) | Retrieves the total elapsed time of the write operation. |
| [IDiscFormat2DataEventArgs::get_RemainingTime](..\imapi2\nf-imapi2-idiscformat2dataeventargs-get_remainingtime.md) | Retrieves the estimated remaining time of the write operation. |
| [IDiscFormat2DataEventArgs::get_TotalTime](..\imapi2\nf-imapi2-idiscformat2dataeventargs-get_totaltime.md) | Retrieves the estimated total time for write operation. |
| [IDiscFormat2Erase::EraseMedia](..\imapi2\nf-imapi2-idiscformat2erase-erasemedia.md) | Erases the media in the active disc recorder. |
| [IDiscFormat2Erase::get_ClientName](..\imapi2\nf-imapi2-idiscformat2erase-get_clientname.md) | Retrieves the friendly name of the client. |
| [IDiscFormat2Erase::get_CurrentPhysicalMediaType](..\imapi2\nf-imapi2-idiscformat2erase-get_currentphysicalmediatype.md) | Retrieves the type of media in the disc device. |
| [IDiscFormat2Erase::get_FullErase](..\imapi2\nf-imapi2-idiscformat2erase-get_fullerase.md) | Determines the quality of the disc erasure. |
| [IDiscFormat2Erase::get_Recorder](..\imapi2\nf-imapi2-idiscformat2erase-get_recorder.md) | Retrieves the recording device to use in the erase operation. |
| [IDiscFormat2Erase::put_ClientName](..\imapi2\nf-imapi2-idiscformat2erase-put_clientname.md) | Sets the friendly name of the client. |
| [IDiscFormat2Erase::put_FullErase](..\imapi2\nf-imapi2-idiscformat2erase-put_fullerase.md) | Determines the quality of the disc erasure. |
| [IDiscFormat2Erase::put_Recorder](..\imapi2\nf-imapi2-idiscformat2erase-put_recorder.md) | Sets the recording device to use in the erase operation. |
| [IDiscFormat2RawCD::CancelWrite](..\imapi2\nf-imapi2-idiscformat2rawcd-cancelwrite.md) | Cancels the current write operation. |
| [IDiscFormat2RawCD::PrepareMedia](..\imapi2\nf-imapi2-idiscformat2rawcd-preparemedia.md) | Locks the current media for exclusive access. |
| [IDiscFormat2RawCD::ReleaseMedia](..\imapi2\nf-imapi2-idiscformat2rawcd-releasemedia.md) | Closes a Disc-At-Once (DAO) writing session of a raw image and releases the lock. |
| [IDiscFormat2RawCD::SetWriteSpeed](..\imapi2\nf-imapi2-idiscformat2rawcd-setwritespeed.md) | Sets the write speed of the disc recorder. |
| [IDiscFormat2RawCD::WriteMedia2](..\imapi2\nf-imapi2-idiscformat2rawcd-writemedia2.md) | Writes a DAO-96 raw image to the blank media using a specified starting address. |
| [IDiscFormat2RawCD::WriteMedia](..\imapi2\nf-imapi2-idiscformat2rawcd-writemedia.md) | Writes a DAO-96 raw image to the blank media using MSF 95 |
| [IDiscFormat2RawCD::get_BufferUnderrunFreeDisabled](..\imapi2\nf-imapi2-idiscformat2rawcd-get_bufferunderrunfreedisabled.md) | Determines if Buffer Underrun Free recording is enabled. |
| [IDiscFormat2RawCD::get_ClientName](..\imapi2\nf-imapi2-idiscformat2rawcd-get_clientname.md) | Retrieves the friendly name of the client. |
| [IDiscFormat2RawCD::get_CurrentPhysicalMediaType](..\imapi2\nf-imapi2-idiscformat2rawcd-get_currentphysicalmediatype.md) | Retrieves the type of media in the disc device. |
| [IDiscFormat2RawCD::get_CurrentRotationTypeIsPureCAV](..\imapi2\nf-imapi2-idiscformat2rawcd-get_currentrotationtypeispurecav.md) | Retrieves the current rotational-speed control used by the recorder. |
| [IDiscFormat2RawCD::get_CurrentWriteSpeed](..\imapi2\nf-imapi2-idiscformat2rawcd-get_currentwritespeed.md) | Retrieves the drive's current write speed. |
| [IDiscFormat2RawCD::get_LastPossibleStartOfLeadout](..\imapi2\nf-imapi2-idiscformat2rawcd-get_lastpossiblestartofleadout.md) | Retrieves the last possible starting position for the leadout area. |
| [IDiscFormat2RawCD::get_Recorder](..\imapi2\nf-imapi2-idiscformat2rawcd-get_recorder.md) | Retrieves the recording device to use for the write operation. |
| [IDiscFormat2RawCD::get_RequestedRotationTypeIsPureCAV](..\imapi2\nf-imapi2-idiscformat2rawcd-get_requestedrotationtypeispurecav.md) | Retrieves the requested rotational-speed control type. |
| [IDiscFormat2RawCD::get_RequestedSectorType](..\imapi2\nf-imapi2-idiscformat2rawcd-get_requestedsectortype.md) | Retrieves the requested data sector to use during write of the stream. |
| [IDiscFormat2RawCD::get_RequestedWriteSpeed](..\imapi2\nf-imapi2-idiscformat2rawcd-get_requestedwritespeed.md) | Retrieves the requested write speed. |
| [IDiscFormat2RawCD::get_StartOfNextSession](..\imapi2\nf-imapi2-idiscformat2rawcd-get_startofnextsession.md) | Retrieves the first sector of the next session. |
| [IDiscFormat2RawCD::get_SupportedSectorTypes](..\imapi2\nf-imapi2-idiscformat2rawcd-get_supportedsectortypes.md) | Retrieves the supported data sector types for the current recorder. |
| [IDiscFormat2RawCD::get_SupportedWriteSpeedDescriptors](..\imapi2\nf-imapi2-idiscformat2rawcd-get_supportedwritespeeddescriptors.md) | Retrieves a list of the detailed write configurations supported by the disc recorder and current media. |
| [IDiscFormat2RawCD::get_SupportedWriteSpeeds](..\imapi2\nf-imapi2-idiscformat2rawcd-get_supportedwritespeeds.md) | Retrieves a list of the write speeds supported by the disc recorder and current media. |
| [IDiscFormat2RawCD::put_BufferUnderrunFreeDisabled](..\imapi2\nf-imapi2-idiscformat2rawcd-put_bufferunderrunfreedisabled.md) | Determines if Buffer Underrun Free recording is enabled. |
| [IDiscFormat2RawCD::put_ClientName](..\imapi2\nf-imapi2-idiscformat2rawcd-put_clientname.md) | Sets the friendly name of the client. |
| [IDiscFormat2RawCD::put_Recorder](..\imapi2\nf-imapi2-idiscformat2rawcd-put_recorder.md) | Sets the recording device to use for the write operation. |
| [IDiscFormat2RawCD::put_RequestedSectorType](..\imapi2\nf-imapi2-idiscformat2rawcd-put_requestedsectortype.md) | Sets the requested data sector to use for writing the stream. |
| [IDiscFormat2RawCDEventArgs::get_CurrentAction](..\imapi2\nf-imapi2-idiscformat2rawcdeventargs-get_currentaction.md) | Retrieves the current write action being performed. |
| [IDiscFormat2RawCDEventArgs::get_ElapsedTime](..\imapi2\nf-imapi2-idiscformat2rawcdeventargs-get_elapsedtime.md) | Retrieves the total elapsed time of the write operation. |
| [IDiscFormat2RawCDEventArgs::get_RemainingTime](..\imapi2\nf-imapi2-idiscformat2rawcdeventargs-get_remainingtime.md) | Retrieves the estimated remaining time of the write operation. |
| [IDiscFormat2TrackAtOnce::AddAudioTrack](..\imapi2\nf-imapi2-idiscformat2trackatonce-addaudiotrack.md) | Writes the data stream to the current media as a new track. |
| [IDiscFormat2TrackAtOnce::CancelAddTrack](..\imapi2\nf-imapi2-idiscformat2trackatonce-canceladdtrack.md) | Cancels the current write operation. |
| [IDiscFormat2TrackAtOnce::PrepareMedia](..\imapi2\nf-imapi2-idiscformat2trackatonce-preparemedia.md) | Locks the current media for exclusive access. |
| [IDiscFormat2TrackAtOnce::ReleaseMedia](..\imapi2\nf-imapi2-idiscformat2trackatonce-releasemedia.md) | Closes the track-writing session and releases the lock. |
| [IDiscFormat2TrackAtOnce::SetWriteSpeed](..\imapi2\nf-imapi2-idiscformat2trackatonce-setwritespeed.md) | Sets the write speed of the disc recorder. |
| [IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_bufferunderrunfreedisabled.md) | Determines if Buffer Underrun Free recording is enabled. |
| [IDiscFormat2TrackAtOnce::get_ClientName](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_clientname.md) | Retrieves the friendly name of the client. |
| [IDiscFormat2TrackAtOnce::get_CurrentPhysicalMediaType](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_currentphysicalmediatype.md) | Retrieves the type of media in the disc device. |
| [IDiscFormat2TrackAtOnce::get_CurrentRotationTypeIsPureCAV](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_currentrotationtypeispurecav.md) | Retrieves the current rotational-speed control used by the recorder. |
| [IDiscFormat2TrackAtOnce::get_CurrentWriteSpeed](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_currentwritespeed.md) | Retrieves the drive's current write speed. |
| [IDiscFormat2TrackAtOnce::get_DoNotFinalizeMedia](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_donotfinalizemedia.md) | Determines if the media is left open for writing after writing the audio track. |
| [IDiscFormat2TrackAtOnce::get_ExpectedTableOfContents](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_expectedtableofcontents.md) | Retrieves the table of content for the audio tracks that were laid on the media within the track-writing session. |
| [IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_freesectorsonmedia.md) | Retrieves the number of sectors available for adding a new track to the media. |
| [IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_numberofexistingtracks.md) | Retrieves the number of existing audio tracks on the media. |
| [IDiscFormat2TrackAtOnce::get_Recorder](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_recorder.md) | Retrieves the recording device to use for the write operation. |
| [IDiscFormat2TrackAtOnce::get_RequestedRotationTypeIsPureCAV](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_requestedrotationtypeispurecav.md) | Retrieves the requested rotational-speed control type. |
| [IDiscFormat2TrackAtOnce::get_RequestedWriteSpeed](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_requestedwritespeed.md) | Retrieves the requested write speed. |
| [IDiscFormat2TrackAtOnce::get_SupportedWriteSpeedDescriptors](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_supportedwritespeeddescriptors.md) | Retrieves a list of the detailed write configurations supported by the disc recorder and current media. |
| [IDiscFormat2TrackAtOnce::get_SupportedWriteSpeeds](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_supportedwritespeeds.md) | Retrieves a list of the write speeds supported by the disc recorder and current media. |
| [IDiscFormat2TrackAtOnce::get_TotalSectorsOnMedia](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_totalsectorsonmedia.md) | Retrieves the total sectors available on the media if writing one continuous audio track. |
| [IDiscFormat2TrackAtOnce::get_UsedSectorsOnMedia](..\imapi2\nf-imapi2-idiscformat2trackatonce-get_usedsectorsonmedia.md) | Retrieves the total number of used sectors on the media. |
| [IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled](..\imapi2\nf-imapi2-idiscformat2trackatonce-put_bufferunderrunfreedisabled.md) | Determines if Buffer Underrun Free Recording is enabled. |
| [IDiscFormat2TrackAtOnce::put_ClientName](..\imapi2\nf-imapi2-idiscformat2trackatonce-put_clientname.md) | Sets the friendly name of the client. |
| [IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia](..\imapi2\nf-imapi2-idiscformat2trackatonce-put_donotfinalizemedia.md) | Determines if the media is left open for writing after writing the audio track. |
| [IDiscFormat2TrackAtOnce::put_Recorder](..\imapi2\nf-imapi2-idiscformat2trackatonce-put_recorder.md) | Sets the recording device to use for the write operation. |
| [IDiscFormat2TrackAtOnceEventArgs::get_CurrentAction](..\imapi2\nf-imapi2-idiscformat2trackatonceeventargs-get_currentaction.md) | Retrieves the current write action being performed. |
| [IDiscFormat2TrackAtOnceEventArgs::get_CurrentTrackNumber](..\imapi2\nf-imapi2-idiscformat2trackatonceeventargs-get_currenttracknumber.md) | Retrieves the current track number being written to the media. |
| [IDiscFormat2TrackAtOnceEventArgs::get_ElapsedTime](..\imapi2\nf-imapi2-idiscformat2trackatonceeventargs-get_elapsedtime.md) | Retrieves the total elapsed time of the write operation. |
| [IDiscFormat2TrackAtOnceEventArgs::get_RemainingTime](..\imapi2\nf-imapi2-idiscformat2trackatonceeventargs-get_remainingtime.md) | Retrieves the estimated remaining time of the write operation. |
| [IDiscMaster2::get_Count](..\imapi2\nf-imapi2-idiscmaster2-get_count.md) | Retrieves the number of the CD and DVD disc devices installed on the computer. |
| [IDiscMaster2::get_IsSupportedEnvironment](..\imapi2\nf-imapi2-idiscmaster2-get_issupportedenvironment.md) | Retrieves a value that determines if the environment contains one or more optical devices and the execution context has permission to access the devices. |
| [IDiscMaster2::get_Item](..\imapi2\nf-imapi2-idiscmaster2-get_item.md) | Retrieves the unique identifier of the specified disc device. |
| [IDiscMaster2::get__NewEnum](..\imapi2\nf-imapi2-idiscmaster2-get__newenum.md) | Retrieves a list of the CD and DVD devices installed on the computer. |
| [IDiscMaster::ClearFormatContent](..\imapi\nf-imapi-idiscmaster-clearformatcontent.md) | Clears the contents of an unburned image (the current stash file). |
| [IDiscMaster::Close](..\imapi\nf-imapi-idiscmaster-close.md) | Closes the interface so other applications can use it. |
| [IDiscMaster::EnumDiscMasterFormats](..\imapi\nf-imapi-idiscmaster-enumdiscmasterformats.md) | Retrieves an enumerator for all disc mastering formats supported by this disc master object. A disc master format specifies the structure of the content in a staged image file (data/audio) and the interface that manages the staged image. |
| [IDiscMaster::EnumDiscRecorders](..\imapi\nf-imapi-idiscmaster-enumdiscrecorders.md) | Retrieves an enumerator for all disc recorders supported by the active disc master format. |
| [IDiscMaster::GetActiveDiscMasterFormat](..\imapi\nf-imapi-idiscmaster-getactivediscmasterformat.md) | Retrieves the active disc recorder format. The active format specifies both the structure of the staged image file content (audio/data) and the COM interface that must be used to manipulate that staged image. |
| [IDiscMaster::GetActiveDiscRecorder](..\imapi\nf-imapi-idiscmaster-getactivediscrecorder.md) | Retrieves an interface pointer to the active disc recorder. The active disc recorder is the recorder where a burn will occur when RecordDisc is called. |
| [IDiscMaster::Open](..\imapi\nf-imapi-idiscmaster-open.md) | Opens an upper-level IMAPI object for access by a client application. |
| [IDiscMaster::ProgressAdvise](..\imapi\nf-imapi-idiscmaster-progressadvise.md) | Registers an application for progress notifications. |
| [IDiscMaster::ProgressUnadvise](..\imapi\nf-imapi-idiscmaster-progressunadvise.md) | Cancels progress notifications for an application. |
| [IDiscMaster::RecordDisc](..\imapi\nf-imapi-idiscmaster-recorddisc.md) | Burns the staged image to media in the active disc recorder. |
| [IDiscMaster::SetActiveDiscMasterFormat](..\imapi\nf-imapi-idiscmaster-setactivediscmasterformat.md) | Sets the currently active disc recorder format. The active format specifies both the structure of the staged image file content (audio/data) and the COM interface that must be used to manipulate that staged image. |
| [IDiscMaster::SetActiveDiscRecorder](..\imapi\nf-imapi-idiscmaster-setactivediscrecorder.md) | Selects an active disc recorder. The active disc recorder is the recorder where a burn will occur when RecordDisc is called. |
| [IDiscMasterProgressEvents::NotifyAddProgress](..\imapi\nf-imapi-idiscmasterprogressevents-notifyaddprogress.md) | Notifies an application of its progress in response to calls to IRedbookDiscMaster |
| [IDiscMasterProgressEvents::NotifyBlockProgress](..\imapi\nf-imapi-idiscmasterprogressevents-notifyblockprogress.md) | Notifies an application of its progress in burning a disc on the active recorder. Notifications are sent for the first and last blocks, and at points in between. |
| [IDiscMasterProgressEvents::NotifyBurnComplete](..\imapi\nf-imapi-idiscmasterprogressevents-notifyburncomplete.md) | Notifies an application that a call to IDiscMaster |
| [IDiscMasterProgressEvents::NotifyClosingDisc](..\imapi\nf-imapi-idiscmasterprogressevents-notifyclosingdisc.md) | Notifies the application that it is has started closing the disc. No further notifications are sent until the burn is finished. |
| [IDiscMasterProgressEvents::NotifyEraseComplete](..\imapi\nf-imapi-idiscmasterprogressevents-notifyerasecomplete.md) | Notifies an application that a call to IDiscRecorder |
| [IDiscMasterProgressEvents::NotifyPnPActivity](..\imapi\nf-imapi-idiscmasterprogressevents-notifypnpactivity.md) | Notifies the application that there is a change to the list of valid disc recorders. (For example, a USB CD-R driver is removed from the system.). |
| [IDiscMasterProgressEvents::NotifyPreparingBurn](..\imapi\nf-imapi-idiscmasterprogressevents-notifypreparingburn.md) | Notifies the application that it is preparing to burn a disc. No further notifications are sent until the burn starts. |
| [IDiscMasterProgressEvents::NotifyTrackProgress](..\imapi\nf-imapi-idiscmasterprogressevents-notifytrackprogress.md) | Notifies an application that a track has started or finished during the burn of an audio disc. |
| [IDiscMasterProgressEvents::QueryCancel](..\imapi\nf-imapi-idiscmasterprogressevents-querycancel.md) | Checks whether an AddData, AddAudioTrackBlocks, or RecordDisc operation should be canceled. |
| [IDiscRecorder2::AcquireExclusiveAccess](..\imapi2\nf-imapi2-idiscrecorder2-acquireexclusiveaccess.md) | Acquires exclusive access to the device. |
| [IDiscRecorder2::CloseTray](..\imapi2\nf-imapi2-idiscrecorder2-closetray.md) | Closes the media tray. |
| [IDiscRecorder2::DisableMcn](..\imapi2\nf-imapi2-idiscrecorder2-disablemcn.md) | Disables Media Change Notification (MCN) for the device. |
| [IDiscRecorder2::EjectMedia](..\imapi2\nf-imapi2-idiscrecorder2-ejectmedia.md) | Ejects media from the device. |
| [IDiscRecorder2::EnableMcn](..\imapi2\nf-imapi2-idiscrecorder2-enablemcn.md) | Enables Media Change Notification (MCN) for the device. |
| [IDiscRecorder2::InitializeDiscRecorder](..\imapi2\nf-imapi2-idiscrecorder2-initializediscrecorder.md) | Associates the object with the specified disc device. |
| [IDiscRecorder2::ReleaseExclusiveAccess](..\imapi2\nf-imapi2-idiscrecorder2-releaseexclusiveaccess.md) | Releases exclusive access to the device. |
| [IDiscRecorder2::get_ActiveDiscRecorder](..\imapi2\nf-imapi2-idiscrecorder2-get_activediscrecorder.md) | Retrieves the unique identifier used to initialize the disc device. |
| [IDiscRecorder2::get_CurrentFeaturePages](..\imapi2\nf-imapi2-idiscrecorder2-get_currentfeaturepages.md) | Retrieves the list of feature pages of the device that are marked as current. |
| [IDiscRecorder2::get_CurrentProfiles](..\imapi2\nf-imapi2-idiscrecorder2-get_currentprofiles.md) | Retrieves all MMC profiles of the device that are marked as current. |
| [IDiscRecorder2::get_DeviceCanLoadMedia](..\imapi2\nf-imapi2-idiscrecorder2-get_devicecanloadmedia.md) | Determines if the device can eject and subsequently reload media. |
| [IDiscRecorder2::get_ExclusiveAccessOwner](..\imapi2\nf-imapi2-idiscrecorder2-get_exclusiveaccessowner.md) | Retrieves the name of the client application that has exclusive access to the device. |
| [IDiscRecorder2::get_LegacyDeviceNumber](..\imapi2\nf-imapi2-idiscrecorder2-get_legacydevicenumber.md) | Retrieves the legacy device number for a CD or DVD device. |
| [IDiscRecorder2::get_ProductId](..\imapi2\nf-imapi2-idiscrecorder2-get_productid.md) | Retrieves the product ID of the device. |
| [IDiscRecorder2::get_ProductRevision](..\imapi2\nf-imapi2-idiscrecorder2-get_productrevision.md) | Retrieves the product revision code of the device. |
| [IDiscRecorder2::get_SupportedFeaturePages](..\imapi2\nf-imapi2-idiscrecorder2-get_supportedfeaturepages.md) | Retrieves the list of features that the device supports. |
| [IDiscRecorder2::get_SupportedModePages](..\imapi2\nf-imapi2-idiscrecorder2-get_supportedmodepages.md) | Retrieves the list of MMC mode pages that the device supports. |
| [IDiscRecorder2::get_SupportedProfiles](..\imapi2\nf-imapi2-idiscrecorder2-get_supportedprofiles.md) | Retrieves the list of MMC profiles that the device supports. |
| [IDiscRecorder2::get_VendorId](..\imapi2\nf-imapi2-idiscrecorder2-get_vendorid.md) | Retrieves the vendor ID for the device. |
| [IDiscRecorder2::get_VolumeName](..\imapi2\nf-imapi2-idiscrecorder2-get_volumename.md) | Retrieves the unique volume name associated with the device. |
| [IDiscRecorder2::get_VolumePathNames](..\imapi2\nf-imapi2-idiscrecorder2-get_volumepathnames.md) | Retrieves a list of drive letters and NTFS mount points for the device. |
| [IDiscRecorder2Ex::GetAdapterDescriptor](..\imapi2\nf-imapi2-idiscrecorder2ex-getadapterdescriptor.md) | Retrieves the adapter descriptor for the device. |
| [IDiscRecorder2Ex::GetByteAlignmentMask](..\imapi2\nf-imapi2-idiscrecorder2ex-getbytealignmentmask.md) | Retrieves the byte alignment mask for the device. |
| [IDiscRecorder2Ex::GetDeviceDescriptor](..\imapi2\nf-imapi2-idiscrecorder2ex-getdevicedescriptor.md) | Retrieves the device descriptor for the device. |
| [IDiscRecorder2Ex::GetDiscInformation](..\imapi2\nf-imapi2-idiscrecorder2ex-getdiscinformation.md) | Retrieves the disc information from the media. |
| [IDiscRecorder2Ex::GetFeaturePage](..\imapi2\nf-imapi2-idiscrecorder2ex-getfeaturepage.md) | Retrieves the specified feature page from the device. |
| [IDiscRecorder2Ex::GetMaximumNonPageAlignedTransferSize](..\imapi2\nf-imapi2-idiscrecorder2ex-getmaximumnonpagealignedtransfersize.md) | Retrieves the maximum non-page-aligned transfer size for the device. |
| [IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize](..\imapi2\nf-imapi2-idiscrecorder2ex-getmaximumpagealignedtransfersize.md) | Retrieves the maximum page-aligned transfer size for the device. |
| [IDiscRecorder2Ex::GetModePage](..\imapi2\nf-imapi2-idiscrecorder2ex-getmodepage.md) | Retrieves the specified mode page from the device. |
| [IDiscRecorder2Ex::GetSupportedFeaturePages](..\imapi2\nf-imapi2-idiscrecorder2ex-getsupportedfeaturepages.md) | Retrieves the list of supported feature pages or the current feature pages of the device. |
| [IDiscRecorder2Ex::GetSupportedModePages](..\imapi2\nf-imapi2-idiscrecorder2ex-getsupportedmodepages.md) | Retrieves the supported mode pages for the device. |
| [IDiscRecorder2Ex::GetSupportedProfiles](..\imapi2\nf-imapi2-idiscrecorder2ex-getsupportedprofiles.md) | Retrieves the supported profiles or the current profiles of the device. |
| [IDiscRecorder2Ex::GetTrackInformation](..\imapi2\nf-imapi2-idiscrecorder2ex-gettrackinformation.md) | Retrieves the track information from the media. |
| [IDiscRecorder2Ex::ReadDvdStructure](..\imapi2\nf-imapi2-idiscrecorder2ex-readdvdstructure.md) | Reads a DVD structure from the media. |
| [IDiscRecorder2Ex::SendCommandGetDataFromDevice](..\imapi2\nf-imapi2-idiscrecorder2ex-sendcommandgetdatafromdevice.md) | Sends a MMC command to the recording device requesting data from the device. |
| [IDiscRecorder2Ex::SendCommandNoData](..\imapi2\nf-imapi2-idiscrecorder2ex-sendcommandnodata.md) | Sends a MMC command to the recording device. Use this function when no data buffer is sent to nor received from the device. |
| [IDiscRecorder2Ex::SendCommandSendDataToDevice](..\imapi2\nf-imapi2-idiscrecorder2ex-sendcommandsenddatatodevice.md) | Sends a MMC command and its associated data buffer to the recording device. |
| [IDiscRecorder2Ex::SendDvdStructure](..\imapi2\nf-imapi2-idiscrecorder2ex-senddvdstructure.md) | Sends a DVD structure to the media. |
| [IDiscRecorder2Ex::SetModePage](..\imapi2\nf-imapi2-idiscrecorder2ex-setmodepage.md) | Sets the mode page data for the device. |
| [IDiscRecorder::Close](..\imapi\nf-imapi-idiscrecorder-close.md) | Releases exclusive access to a disc recorder. This restores file system access to the drive. |
| [IDiscRecorder::Eject](..\imapi\nf-imapi-idiscrecorder-eject.md) | Unlocks and ejects the tray of the disc recorder, if possible. |
| [IDiscRecorder::Erase](..\imapi\nf-imapi-idiscrecorder-erase.md) | Attempts to erase the CD-RW media if this is a CD-RW disc recorder. Both full and quick erases are supported. |
| [IDiscRecorder::GetBasePnPID](..\imapi\nf-imapi-idiscrecorder-getbasepnpid.md) | Retrieves a base PnP string that can be used to consistently identify a specific class of device by make and model. The string can be used by applications to customize their behavior according to the specific recorder type. |
| [IDiscRecorder::GetDisplayNames](..\imapi\nf-imapi-idiscrecorder-getdisplaynames.md) | Retrieves a formatted name for the recorder that can be displayed. The name consists of the manufacturer and product identifier of the device. |
| [IDiscRecorder::GetPath](..\imapi\nf-imapi-idiscrecorder-getpath.md) | Retrieves a path to the device within the operating system. This path should be used in conjunction with the display name to completely identify an available disc recorder. |
| [IDiscRecorder::GetRecorderGUID](..\imapi\nf-imapi-idiscrecorder-getrecorderguid.md) | Retrieves the GUID of the physical disc recorder currently associated with the recorder object. |
| [IDiscRecorder::GetRecorderProperties](..\imapi\nf-imapi-idiscrecorder-getrecorderproperties.md) | Retrieves a pointer to an IPropertyStorage interface. |
| [IDiscRecorder::GetRecorderState](..\imapi\nf-imapi-idiscrecorder-getrecorderstate.md) | Retrieves the disc recorder state. |
| [IDiscRecorder::GetRecorderType](..\imapi\nf-imapi-idiscrecorder-getrecordertype.md) | Determines whether the disc recorder is a CD-R or CD-RW type device. This does not indicate the type of media that is currently inserted in the device. |
| [IDiscRecorder::OpenExclusive](..\imapi\nf-imapi-idiscrecorder-openexclusive.md) | Opens a disc recorder for exclusive access. |
| [IDiscRecorder::QueryMediaInfo](..\imapi\nf-imapi-idiscrecorder-querymediainfo.md) | Retrieves information about the currently mounted media, such as the total number of blocks used on the media. |
| [IDiscRecorder::QueryMediaType](..\imapi\nf-imapi-idiscrecorder-querymediatype.md) | Detects the type of media currently inserted in the recorder, if any. |
| [IDiscRecorder::SetRecorderProperties](..\imapi\nf-imapi-idiscrecorder-setrecorderproperties.md) | Accepts an IPropertyStorage pointer for an object with all the properties that the application wishes to change. Sparse settings are supported. |
| [IEnumFsiItems::Clone](..\imapi2fs\nf-imapi2fs-ienumfsiitems-clone.md) | Creates another enumerator that contains the same enumeration state as the current one. |
| [IEnumFsiItems::Next](..\imapi2fs\nf-imapi2fs-ienumfsiitems-next.md) | Retrieves a specified number of items in the enumeration sequence. |
| [IEnumFsiItems::Reset](..\imapi2fs\nf-imapi2fs-ienumfsiitems-reset.md) | Resets the enumeration sequence to the beginning. |
| [IEnumFsiItems::Skip](..\imapi2fs\nf-imapi2fs-ienumfsiitems-skip.md) | Skips a specified number of items in the enumeration sequence. |
| [IEnumProgressItems::Clone](..\imapi2fs\nf-imapi2fs-ienumprogressitems-clone.md) | Creates another enumerator that contains the same enumeration state as the current one. |
| [IEnumProgressItems::Next](..\imapi2fs\nf-imapi2fs-ienumprogressitems-next.md) | Retrieves a specified number of items in the enumeration sequence. |
| [IEnumProgressItems::Reset](..\imapi2fs\nf-imapi2fs-ienumprogressitems-reset.md) | Resets the enumeration sequence to the beginning. |
| [IEnumProgressItems::Skip](..\imapi2fs\nf-imapi2fs-ienumprogressitems-skip.md) | Skips a specified number of items in the enumeration sequence. |
| [IFileSystemImage2::get_BootImageOptionsArray](..\imapi2fs\nf-imapi2fs-ifilesystemimage2-get_bootimageoptionsarray.md) | Retrieves the boot option array that will be utilized to generate the file system image. |
| [IFileSystemImage2::put_BootImageOptionsArray](..\imapi2fs\nf-imapi2fs-ifilesystemimage2-put_bootimageoptionsarray.md) | Sets the boot option array that will be utilized to generate the file system image. Unlike IFileSystemImage |
| [IFileSystemImage3::ProbeSpecificFileSystem](..\imapi2fs\nf-imapi2fs-ifilesystemimage3-probespecificfilesystem.md) | Determines if a specific file system on the current media is appendable through the IMAPI. |
| [IFileSystemImage3::get_CreateRedundantUdfMetadataFiles](..\imapi2fs\nf-imapi2fs-ifilesystemimage3-get_createredundantudfmetadatafiles.md) | Retrieves a property value that specifies if the UDF Metadata will be redundant in the file system image. |
| [IFileSystemImage3::put_CreateRedundantUdfMetadataFiles](..\imapi2fs\nf-imapi2fs-ifilesystemimage3-put_createredundantudfmetadatafiles.md) | Sets the property that specifies if the UDF Metadata will be redundant in the file system image. |
| [IFileSystemImage::CalculateDiscIdentifier](..\imapi2fs\nf-imapi2fs-ifilesystemimage-calculatediscidentifier.md) | Retrieves a string that identifies a disc and the sessions recorded on the disc. |
| [IFileSystemImage::ChooseImageDefaultsForMediaType](..\imapi2fs\nf-imapi2fs-ifilesystemimage-chooseimagedefaultsformediatype.md) | Sets the default file system types and the image size based on the specified media type. |
| [IFileSystemImage::ChooseImageDefaults](..\imapi2fs\nf-imapi2fs-ifilesystemimage-chooseimagedefaults.md) | Sets the default file system types and the image size based on the current media. |
| [IFileSystemImage::CreateDirectoryItem](..\imapi2fs\nf-imapi2fs-ifilesystemimage-createdirectoryitem.md) | Create a directory item with the specified name. |
| [IFileSystemImage::CreateFileItem](..\imapi2fs\nf-imapi2fs-ifilesystemimage-createfileitem.md) | Create a file item with the specified name. |
| [IFileSystemImage::CreateResultImage](..\imapi2fs\nf-imapi2fs-ifilesystemimage-createresultimage.md) | Create the result object that contains the file system and file data. |
| [IFileSystemImage::Exists](..\imapi2fs\nf-imapi2fs-ifilesystemimage-exists.md) | Checks for the existence of a given file or directory. |
| [IFileSystemImage::GetDefaultFileSystemForImport](..\imapi2fs\nf-imapi2fs-ifilesystemimage-getdefaultfilesystemforimport.md) | Retrieves the file system to import by default. |
| [IFileSystemImage::IdentifyFileSystemsOnDisc](..\imapi2fs\nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc.md) | Retrieves a list of the different types of file systems on the optical media. |
| [IFileSystemImage::ImportFileSystem](..\imapi2fs\nf-imapi2fs-ifilesystemimage-importfilesystem.md) | Imports the default file system on the current disc. |
| [IFileSystemImage::ImportSpecificFileSystem](..\imapi2fs\nf-imapi2fs-ifilesystemimage-importspecificfilesystem.md) | Import a specific file system from disc. |
| [IFileSystemImage::LockInChangePoint](..\imapi2fs\nf-imapi2fs-ifilesystemimage-lockinchangepoint.md) | Locks the file system information at the current change-point level. |
| [IFileSystemImage::RollbackToChangePoint](..\imapi2fs\nf-imapi2fs-ifilesystemimage-rollbacktochangepoint.md) | Reverts the image back to the specified change point. |
| [IFileSystemImage::SetMaxMediaBlocksFromDevice](..\imapi2fs\nf-imapi2fs-ifilesystemimage-setmaxmediablocksfromdevice.md) | Set maximum number of blocks available based on the capabilities of the recorder. |
| [IFileSystemImage::get_BootImageOptions](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_bootimageoptions.md) | Retrieves the boot image that you want to add to the file system image. |
| [IFileSystemImage::get_ChangePoint](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_changepoint.md) | Retrieves the change point identifier. |
| [IFileSystemImage::get_DirectoryCount](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_directorycount.md) | Retrieves the number of directories in the file system image. |
| [IFileSystemImage::get_FileCount](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_filecount.md) | Retrieves the number of files in the file system image. |
| [IFileSystemImage::get_FileSystemsSupported](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_filesystemssupported.md) | Retrieves the list of file system types that a client can use to build a file system image. |
| [IFileSystemImage::get_FileSystemsToCreate](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_filesystemstocreate.md) | Retrieves the types of file systems to create when generating the result stream. |
| [IFileSystemImage::get_FreeMediaBlocks](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_freemediablocks.md) | Retrieves the maximum number of blocks available for the image. |
| [IFileSystemImage::get_ISO9660InterchangeLevel](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevel.md) | Retrieves the ISO9660 compatibility level to use when creating the result image. |
| [IFileSystemImage::get_ISO9660InterchangeLevelsSupported](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevelssupported.md) | Retrieves the supported ISO9660 compatibility levels. |
| [IFileSystemImage::get_ImportedVolumeName](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_importedvolumename.md) | Retrieves the volume name provided from an imported file system. |
| [IFileSystemImage::get_MultisessionInterfaces](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces.md) | Retrieves the list of multi-session interfaces for the optical media. |
| [IFileSystemImage::get_Root](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_root.md) | Retrieves the root directory item. |
| [IFileSystemImage::get_SessionStartBlock](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_sessionstartblock.md) | Retrieves the starting block address for the recording session. |
| [IFileSystemImage::get_StageFiles](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_stagefiles.md) | Indicates if the files being added to the file system image should be staged before the burn. |
| [IFileSystemImage::get_StrictFileSystemCompliance](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_strictfilesystemcompliance.md) | Determines the compliance level for creating and developing the file-system image. |
| [IFileSystemImage::get_UDFRevision](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_udfrevision.md) | Retrieves the UDF revision level of the imported file system image. |
| [IFileSystemImage::get_UDFRevisionsSupported](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_udfrevisionssupported.md) | Retrieves a list of supported UDF revision levels. |
| [IFileSystemImage::get_UseRestrictedCharacterSet](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_userestrictedcharacterset.md) | Determines if the file and directory names use a restricted character. |
| [IFileSystemImage::get_UsedBlocks](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_usedblocks.md) | Retrieves the number of blocks in use. |
| [IFileSystemImage::get_VolumeNameISO9660](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_volumenameiso9660.md) | Retrieves the volume name for the ISO9660 system image. |
| [IFileSystemImage::get_VolumeNameJoliet](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_volumenamejoliet.md) | Retrieves the volume name for the Joliet system image. |
| [IFileSystemImage::get_VolumeNameUDF](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_volumenameudf.md) | Retrieves the volume name for the UDF system image. |
| [IFileSystemImage::get_VolumeName](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_volumename.md) | Retrieves the volume name for this file system image. |
| [IFileSystemImage::get_WorkingDirectory](..\imapi2fs\nf-imapi2fs-ifilesystemimage-get_workingdirectory.md) | Retrieves the temporary directory in which stash files are built. |
| [IFileSystemImage::put_BootImageOptions](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_bootimageoptions.md) | Sets the boot image that you want to add to the file-system image. This method creates a complete copy of the passed-in boot options by copying the stream from the supplied IBootOptions interface. |
| [IFileSystemImage::put_FileSystemsToCreate](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_filesystemstocreate.md) | Sets the file systems to create when generating the result stream. |
| [IFileSystemImage::put_FreeMediaBlocks](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_freemediablocks.md) | Sets the maximum number of blocks available for the image. |
| [IFileSystemImage::put_ISO9660InterchangeLevel](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_iso9660interchangelevel.md) | Sets the ISO9660 compatibility level of the file system image. |
| [IFileSystemImage::put_MultisessionInterfaces](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces.md) | Sets the list of multi-session interfaces for the optical media. |
| [IFileSystemImage::put_SessionStartBlock](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_sessionstartblock.md) | Sets the starting block address for the recording session. |
| [IFileSystemImage::put_StageFiles](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_stagefiles.md) | Determines if the files being added to the file system image should be staged before the burn. |
| [IFileSystemImage::put_StrictFileSystemCompliance](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_strictfilesystemcompliance.md) | Determines the compliance level for creating and developing the file-system image. |
| [IFileSystemImage::put_UDFRevision](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_udfrevision.md) | Sets the UDF revision level of the file system image. |
| [IFileSystemImage::put_UseRestrictedCharacterSet](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_userestrictedcharacterset.md) | Determines if file and directory names should be restricted to using only CP_ANSI characters. |
| [IFileSystemImage::put_VolumeName](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_volumename.md) | Sets the volume name for this file system image. |
| [IFileSystemImage::put_WorkingDirectory](..\imapi2fs\nf-imapi2fs-ifilesystemimage-put_workingdirectory.md) | Sets the temporary directory in which stash files are built. |
| [IFileSystemImageResult2::get_ModifiedBlocks](..\imapi2fs\nf-imapi2fs-ifilesystemimageresult2-get_modifiedblocks.md) | Retrieves the list of modified blocks in the result image. |
| [IFileSystemImageResult::get_BlockSize](..\imapi2fs\nf-imapi2fs-ifilesystemimageresult-get_blocksize.md) | Retrieves the size, in bytes, of a block of data. |
| [IFileSystemImageResult::get_DiscId](..\imapi2fs\nf-imapi2fs-ifilesystemimageresult-get_discid.md) | Retrieves the disc volume name for this file system image. |
| [IFileSystemImageResult::get_ImageStream](..\imapi2fs\nf-imapi2fs-ifilesystemimageresult-get_imagestream.md) | Retrieves the burn image stream. |
| [IFileSystemImageResult::get_ProgressItems](..\imapi2fs\nf-imapi2fs-ifilesystemimageresult-get_progressitems.md) | Retrieves the progress item block mapping collection. |
| [IFileSystemImageResult::get_TotalBlocks](..\imapi2fs\nf-imapi2fs-ifilesystemimageresult-get_totalblocks.md) | Retrieves the number of blocks in the result image. |
| [IFsiDirectoryItem2::AddTreeWithNamedStreams](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem2-addtreewithnamedstreams.md) | Adds the contents of a directory tree along with named streams associated with all files to the file system image. |
| [IFsiDirectoryItem::AddDirectory](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-adddirectory.md) | Adds a directory to the file system image. |
| [IFsiDirectoryItem::AddFile](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-addfile.md) | Adds a file to the file system image. |
| [IFsiDirectoryItem::AddTree](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-addtree.md) | Adds the contents of a directory tree to the file system image. |
| [IFsiDirectoryItem::Add](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-add.md) | Adds a file or directory described by the IFsiItem object to the file system image. |
| [IFsiDirectoryItem::RemoveTree](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-removetree.md) | Remove the specified directory tree from the file system image. |
| [IFsiDirectoryItem::Remove](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-remove.md) | Removes the specified item from the file system image. |
| [IFsiDirectoryItem::get_Count](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-get_count.md) | Number of child items in the enumeration. |
| [IFsiDirectoryItem::get_EnumFsiItems](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-get_enumfsiitems.md) | Retrieves a list of child items contained within the directory in the file system image. |
| [IFsiDirectoryItem::get_Item](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-get_item.md) | Retrieves the specified directory or file item from file system image. |
| [IFsiDirectoryItem::get__NewEnum](..\imapi2fs\nf-imapi2fs-ifsidirectoryitem-get__newenum.md) | Retrieves a list of child items contained within the directory in the file system image. |
| [IFsiFileItem2::AddStream](..\imapi2fs\nf-imapi2fs-ifsifileitem2-addstream.md) | Associates a named stream with a specific file in the file system image. |
| [IFsiFileItem2::RemoveStream](..\imapi2fs\nf-imapi2fs-ifsifileitem2-removestream.md) | Removes a named stream association with a file. |
| [IFsiFileItem2::get_FsiNamedStreams](..\imapi2fs\nf-imapi2fs-ifsifileitem2-get_fsinamedstreams.md) | Retrieves a collection of named streams associated with a file in the file system image. |
| [IFsiFileItem2::get_IsNamedStream](..\imapi2fs\nf-imapi2fs-ifsifileitem2-get_isnamedstream.md) | Determines if the item is a named stream. |
| [IFsiFileItem2::get_IsRealTime](..\imapi2fs\nf-imapi2fs-ifsifileitem2-get_isrealtime.md) | Retrieves the property value that specifies if a file item in the file system image is a 'Real-Time' or standard file. |
| [IFsiFileItem2::put_IsRealTime](..\imapi2fs\nf-imapi2fs-ifsifileitem2-put_isrealtime.md) | Sets the 'Real-Time' attribute of a file in a file system. This attribute specifies whether or not the content requires a minimum data-transfer rate when writing or reading, for example, audio and video data. |
| [IFsiFileItem::get_DataSize32BitHigh](..\imapi2fs\nf-imapi2fs-ifsifileitem-get_datasize32bithigh.md) | Retrieves the most significant 32 bits of the IFsiFileItem |
| [IFsiFileItem::get_DataSize32BitLow](..\imapi2fs\nf-imapi2fs-ifsifileitem-get_datasize32bitlow.md) | Retrieves the least significant 32 bits of the IFsiFileItem |
| [IFsiFileItem::get_DataSize](..\imapi2fs\nf-imapi2fs-ifsifileitem-get_datasize.md) | Retrieves the number of bytes in the file. |
| [IFsiFileItem::get_Data](..\imapi2fs\nf-imapi2fs-ifsifileitem-get_data.md) | Retrieves the data stream of the file's content. |
| [IFsiFileItem::put_Data](..\imapi2fs\nf-imapi2fs-ifsifileitem-put_data.md) | Sets the data stream of the file's content. |
| [IFsiItem::FileSystemName](..\imapi2fs\nf-imapi2fs-ifsiitem-filesystemname.md) | Retrieves the name of the item as modified to conform to the specified file system. |
| [IFsiItem::FileSystemPath](..\imapi2fs\nf-imapi2fs-ifsiitem-filesystempath.md) | Retrieves the full path of the item as modified to conform to the specified file system. |
| [IFsiItem::get_CreationTime](..\imapi2fs\nf-imapi2fs-ifsiitem-get_creationtime.md) | Retrieves the date and time that the directory or file item was created and added to the file system image. |
| [IFsiItem::get_FullPath](..\imapi2fs\nf-imapi2fs-ifsiitem-get_fullpath.md) | Retrieves the full path of the file or directory item in the file system image. |
| [IFsiItem::get_IsHidden](..\imapi2fs\nf-imapi2fs-ifsiitem-get_ishidden.md) | Determines if the item's hidden attribute is set in the file system image. |
| [IFsiItem::get_LastAccessedTime](..\imapi2fs\nf-imapi2fs-ifsiitem-get_lastaccessedtime.md) | Retrieves the date and time the directory or file item was last accessed in the file system image. |
| [IFsiItem::get_LastModifiedTime](..\imapi2fs\nf-imapi2fs-ifsiitem-get_lastmodifiedtime.md) | Retrieves the date and time that the directory or file item was last modified in the file system image. |
| [IFsiItem::get_Name](..\imapi2fs\nf-imapi2fs-ifsiitem-get_name.md) | Retrieves the name of the directory or file item in the file system image. |
| [IFsiItem::put_CreationTime](..\imapi2fs\nf-imapi2fs-ifsiitem-put_creationtime.md) | Sets the date and time that the directory or file item was created and added to the file system image. |
| [IFsiItem::put_IsHidden](..\imapi2fs\nf-imapi2fs-ifsiitem-put_ishidden.md) | Determines if the item's hidden attribute is set in the file system image. |
| [IFsiItem::put_LastAccessedTime](..\imapi2fs\nf-imapi2fs-ifsiitem-put_lastaccessedtime.md) | Sets the date and time that the directory or file item was last accessed in the file system image. |
| [IFsiItem::put_LastModifiedTime](..\imapi2fs\nf-imapi2fs-ifsiitem-put_lastmodifiedtime.md) | Sets the date and time that the item was last modified in the file system image. |
| [IFsiNamedStreams::get_Count](..\imapi2fs\nf-imapi2fs-ifsinamedstreams-get_count.md) | Returns the number of the named streams associated with a file in the file system image. |
| [IFsiNamedStreams::get_EnumNamedStreams](..\imapi2fs\nf-imapi2fs-ifsinamedstreams-get_enumnamedstreams.md) | Creates a non-variant enumerator for the collection of the named streams associated with a file in the file system image. |
| [IFsiNamedStreams::get_Item](..\imapi2fs\nf-imapi2fs-ifsinamedstreams-get_item.md) | Retrieves a single named stream associated with a file in the file system image. |
| [IIsoImageManager::SetPath](..\imapi2fs\nf-imapi2fs-iisoimagemanager-setpath.md) | Sets the Path property value with a logical path to an .iso image. |
| [IIsoImageManager::SetStream](..\imapi2fs\nf-imapi2fs-iisoimagemanager-setstream.md) | Sets the Stream property with the IStream object associated with the .iso image. |
| [IIsoImageManager::Validate](..\imapi2fs\nf-imapi2fs-iisoimagemanager-validate.md) | Determines if the provided .iso image is valid. |
| [IIsoImageManager::get_Path](..\imapi2fs\nf-imapi2fs-iisoimagemanager-get_path.md) | Retrives the logical path to an .iso image. |
| [IIsoImageManager::get_Stream](..\imapi2fs\nf-imapi2fs-iisoimagemanager-get_stream.md) | Retrieves the IStream object associated with the .iso image. |
| [IJolietDiscMaster::AddData](..\imapi\nf-imapi-ijolietdiscmaster-adddata.md) | Adds the contents of a root storage to the staged image file. This storage will be enumerated to place all substorages and streams in the root file system of the stage image file. Substorages become folders and streams become files. |
| [IJolietDiscMaster::GetDataBlockSize](..\imapi\nf-imapi-ijolietdiscmaster-getdatablocksize.md) | Retrieves the size of a data block. |
| [IJolietDiscMaster::GetJolietProperties](..\imapi\nf-imapi-ijolietdiscmaster-getjolietproperties.md) | Retrieves a pointer to an IPropertyStorage interface that contains the Joliet properties. |
| [IJolietDiscMaster::GetTotalDataBlocks](..\imapi\nf-imapi-ijolietdiscmaster-gettotaldatablocks.md) | Retrieves the total number of blocks available for staging a Joliet data disc. |
| [IJolietDiscMaster::GetUsedDataBlocks](..\imapi\nf-imapi-ijolietdiscmaster-getuseddatablocks.md) | Retrieves the total number of data blocks that are in use. |
| [IJolietDiscMaster::SetJolietProperties](..\imapi\nf-imapi-ijolietdiscmaster-setjolietproperties.md) | Sets the Joliet properties. |
| [IMultisession::get_ImportRecorder](..\imapi2\nf-imapi2-imultisession-get_importrecorder.md) | Retrieves the disc recorder to use to import one or more previous sessions. |
| [IMultisession::get_InUse](..\imapi2\nf-imapi2-imultisession-get_inuse.md) | Determines if this multi-session interface is the one you should use on the current media. |
| [IMultisession::get_IsSupportedOnCurrentMediaState](..\imapi2\nf-imapi2-imultisession-get_issupportedoncurrentmediastate.md) | Determines if the multi-session type can write to the current optical media. |
| [IMultisession::put_InUse](..\imapi2\nf-imapi2-imultisession-put_inuse.md) | Determines if this multi-session interface is the one you should use on the current media. |
| [IMultisessionRandomWrite::get_LastWrittenAddress](..\imapi2\nf-imapi2-imultisessionrandomwrite-get_lastwrittenaddress.md) | Retrieves the last written address on the media. |
| [IMultisessionRandomWrite::get_TotalSectorsOnMedia](..\imapi2\nf-imapi2-imultisessionrandomwrite-get_totalsectorsonmedia.md) | Retrieves the total number of sectors on the media. |
| [IMultisessionRandomWrite::get_WriteUnitSize](..\imapi2\nf-imapi2-imultisessionrandomwrite-get_writeunitsize.md) | Retrieves the size of a writeable unit on the media. |
| [IMultisessionSequential2::get_WriteUnitSize](..\imapi2\nf-imapi2-imultisessionsequential2-get_writeunitsize.md) | Retrieves the size of a writeable unit on the media. |
| [IMultisessionSequential::get_FreeSectorsOnMedia](..\imapi2\nf-imapi2-imultisessionsequential-get_freesectorsonmedia.md) | Retrieves the number of free sectors available on the media. |
| [IMultisessionSequential::get_IsFirstDataSession](..\imapi2\nf-imapi2-imultisessionsequential-get_isfirstdatasession.md) | Determines if this session is the first data session on the media. |
| [IMultisessionSequential::get_LastWrittenAddressOfPreviousSession](..\imapi2\nf-imapi2-imultisessionsequential-get_lastwrittenaddressofprevioussession.md) | Retrieves the last sector written in the previous session on the media. |
| [IMultisessionSequential::get_NextWritableAddress](..\imapi2\nf-imapi2-imultisessionsequential-get_nextwritableaddress.md) | Retrieves the next writable address on the media, including used sectors. |
| [IMultisessionSequential::get_StartAddressOfPreviousSession](..\imapi2\nf-imapi2-imultisessionsequential-get_startaddressofprevioussession.md) | Retrieves the first sector written in the previous session on the media. |
| [IProgressItem::get_BlockCount](..\imapi2fs\nf-imapi2fs-iprogressitem-get_blockcount.md) | Retrieves the number of blocks in the progress item. |
| [IProgressItem::get_Description](..\imapi2fs\nf-imapi2fs-iprogressitem-get_description.md) | Retrieves the description in the progress item. |
| [IProgressItem::get_FirstBlock](..\imapi2fs\nf-imapi2fs-iprogressitem-get_firstblock.md) | Retrieves the first block number in this segment of the result image. |
| [IProgressItem::get_LastBlock](..\imapi2fs\nf-imapi2fs-iprogressitem-get_lastblock.md) | Retrieves the last block in this segment of the result image. |
| [IProgressItems::ProgressItemFromBlock](..\imapi2fs\nf-imapi2fs-iprogressitems-progressitemfromblock.md) | Retrieves a progress item based on the specified block number. |
| [IProgressItems::ProgressItemFromDescription](..\imapi2fs\nf-imapi2fs-iprogressitems-progressitemfromdescription.md) | Retrieves a progress item based on the specified file name. |
| [IProgressItems::get_Count](..\imapi2fs\nf-imapi2fs-iprogressitems-get_count.md) | Retrieves the number of progress items in the collection. |
| [IProgressItems::get_EnumProgressItems](..\imapi2fs\nf-imapi2fs-iprogressitems-get_enumprogressitems.md) | Retrieves the list of progress items from the collection. |
| [IProgressItems::get_Item](..\imapi2fs\nf-imapi2fs-iprogressitems-get_item.md) | Retrieves the specified progress item from the collection. |
| [IProgressItems::get__NewEnum](..\imapi2fs\nf-imapi2fs-iprogressitems-get__newenum.md) | Retrieves the list of progress items from the collection. |
| [IRawCDImageCreator::AddSpecialPregap](..\imapi2\nf-imapi2-irawcdimagecreator-addspecialpregap.md) | Accepts the provided IStream object and saves the associated pointer to be used as data for the pre-gap for track 1. |
| [IRawCDImageCreator::AddSubcodeRWGenerator](..\imapi2\nf-imapi2-irawcdimagecreator-addsubcoderwgenerator.md) | Allows the addition of custom R-W subcode, provided by the IStream. The provided object must have a size equal to the number of sectors in the raw disc image * 96 bytes when the final image is created. |
| [IRawCDImageCreator::AddTrack](..\imapi2\nf-imapi2-irawcdimagecreator-addtrack.md) | Accepts the provided IStream object and saves the interface pointer as the next track in the image. |
| [IRawCDImageCreator::CreateResultImage](..\imapi2\nf-imapi2-irawcdimagecreator-createresultimage.md) | Creates the final IStream object based on the current settings. |
| [IRawCDImageCreator::get_DisableGaplessAudio](..\imapi2\nf-imapi2-irawcdimagecreator-get_disablegaplessaudio.md) | Retrieves the current value that specifies if &#0034;Gapless Audio&#0034; recording is disabled. This property defaults to a value of VARIANT_FALSE, which disables the use of &#0034;gapless&#0034; recording between consecutive audio tracks. |
| [IRawCDImageCreator::get_ExpectedTableOfContents](..\imapi2\nf-imapi2-irawcdimagecreator-get_expectedtableofcontents.md) | Gets the SCSI-form table of contents for the resulting disc. |
| [IRawCDImageCreator::get_LastUsedUserSectorInImage](..\imapi2\nf-imapi2-irawcdimagecreator-get_lastusedusersectorinimage.md) | Retrieves the number of total used sectors on the current media, including any overhead between existing tracks. |
| [IRawCDImageCreator::get_MediaCatalogNumber](..\imapi2\nf-imapi2-irawcdimagecreator-get_mediacatalognumber.md) | Sets the Media Catalog Number (MCN) for the entire audio disc. |
| [IRawCDImageCreator::get_NumberOfExistingTracks](..\imapi2\nf-imapi2-irawcdimagecreator-get_numberofexistingtracks.md) | Retrieves the number of existing audio tracks on the media. |
| [IRawCDImageCreator::get_ResultingImageType](..\imapi2\nf-imapi2-irawcdimagecreator-get_resultingimagetype.md) | Retrieves the value that specifies the type of image file that will be generated. |
| [IRawCDImageCreator::get_StartOfLeadoutLimit](..\imapi2\nf-imapi2-irawcdimagecreator-get_startofleadoutlimit.md) | Retrieves the current StartOfLeadoutLimit property value. This value specifies if the resulting image is required to fit on a piece of media with a StartOfLeadout greater than or equal to the LBA. |
| [IRawCDImageCreator::get_StartOfLeadout](..\imapi2\nf-imapi2-irawcdimagecreator-get_startofleadout.md) | Retrieves the value that defines the LBA for the start of the Leadout. This method can be utilized to determine if the image can be written to a piece of media by comparing it against the LastPossibleStartOfLeadout for the media. |
| [IRawCDImageCreator::get_StartingTrackNumber](..\imapi2\nf-imapi2-irawcdimagecreator-get_startingtracknumber.md) | Retrieves the starting track number. |
| [IRawCDImageCreator::get_TrackInfo](..\imapi2\nf-imapi2-irawcdimagecreator-get_trackinfo.md) | Retrieves an indexed property, which takes a LONG value with a range of 1 to 99 as the index to determine which track the user is querying. The returned object is then queried/set for the particular per-track property of interest. |
| [IRawCDImageCreator::put_DisableGaplessAudio](..\imapi2\nf-imapi2-irawcdimagecreator-put_disablegaplessaudio.md) | Sets the value that specifies if &#0034;Gapless Audio&#0034; recording is disabled. This property defaults to a value of VARIANT_FALSE, which disables the use of &#0034;gapless&#0034; recording between consecutive audio tracks. |
| [IRawCDImageCreator::put_MediaCatalogNumber](..\imapi2\nf-imapi2-irawcdimagecreator-put_mediacatalognumber.md) | Retrieves the Media Catalog Number (MCN) for the entire audio disc. |
| [IRawCDImageCreator::put_ResultingImageType](..\imapi2\nf-imapi2-irawcdimagecreator-put_resultingimagetype.md) | Sets the value that defines the type of image file that will be generated. |
| [IRawCDImageCreator::put_StartOfLeadoutLimit](..\imapi2\nf-imapi2-irawcdimagecreator-put_startofleadoutlimit.md) | Sets the StartOfLeadoutLimit property value. |
| [IRawCDImageCreator::put_StartingTrackNumber](..\imapi2\nf-imapi2-irawcdimagecreator-put_startingtracknumber.md) | Sets the starting track number. |
| [IRawCDImageTrackInfo::get_AudioHasPreemphasis](..\imapi2\nf-imapi2-irawcdimagetrackinfo-get_audiohaspreemphasis.md) | Retrieves the value that specifies if an audio track has an additional pre-emphasis added to the audio data. |
| [IRawCDImageTrackInfo::get_DigitalAudioCopySetting](..\imapi2\nf-imapi2-irawcdimagetrackinfo-get_digitalaudiocopysetting.md) | Retrieves the value for the bit that represents the current digital audio copy setting on the resulting media. Please see the IMAPI_CD_TRACK_DIGITAL_COPY_SETTING enumeration for possible values. |
| [IRawCDImageTrackInfo::get_ISRC](..\imapi2\nf-imapi2-irawcdimagetrackinfo-get_isrc.md) | Retrieves the International Standard Recording Code (ISRC) currently associated with the track. This property value defaults to NULL (or a zero-length string) and may only be set for tracks containing audio data. |
| [IRawCDImageTrackInfo::get_SectorCount](..\imapi2\nf-imapi2-irawcdimagetrackinfo-get_sectorcount.md) | Retrieves the number of user sectors in this track. |
| [IRawCDImageTrackInfo::get_SectorType](..\imapi2\nf-imapi2-irawcdimagetrackinfo-get_sectortype.md) | Retrieves the type of data provided for the sectors in this track. For more detail on the possible sector types, see IMAPI_CD_SECTOR_TYPE. |
| [IRawCDImageTrackInfo::get_StartingLba](..\imapi2\nf-imapi2-irawcdimagetrackinfo-get_startinglba.md) | Retrieves the LBA of the first user sectors in this track. |
| [IRawCDImageTrackInfo::get_TrackIndexes](..\imapi2\nf-imapi2-irawcdimagetrackinfo-get_trackindexes.md) | Retrieves the one-based index of the tracks on the disc. |
| [IRawCDImageTrackInfo::get_TrackNumber](..\imapi2\nf-imapi2-irawcdimagetrackinfo-get_tracknumber.md) | Retrieves the track number for this track. |
| [IRawCDImageTrackInfo::put_AudioHasPreemphasis](..\imapi2\nf-imapi2-irawcdimagetrackinfo-put_audiohaspreemphasis.md) | Sets the value that specifies if an audio track has an additional pre-emphasis added to the audio data prior to being written to CD. |
| [IRawCDImageTrackInfo::put_DigitalAudioCopySetting](..\imapi2\nf-imapi2-irawcdimagetrackinfo-put_digitalaudiocopysetting.md) | Sets the digital audio copy &#0034;Allowed&#0034; bit to one of three values on the resulting media. Please see the IMAPI_CD_TRACK_DIGITAL_COPY_SETTING enumeration for additional information on each possible value. |
| [IRawCDImageTrackInfo::put_ISRC](..\imapi2\nf-imapi2-irawcdimagetrackinfo-put_isrc.md) | Sets the International Standard Recording Code (ISRC) currently associated with the track. This property value defaults to NULL (or a zero-length string) and may only be set for tracks containing audio data. |
| [IRedbookDiscMaster::AddAudioTrackBlocks](..\imapi\nf-imapi-iredbookdiscmaster-addaudiotrackblocks.md) | Adds blocks of audio data to the currently open track. This method can be called repeatedly until there is no space available or the track is full. |
| [IRedbookDiscMaster::CloseAudioTrack](..\imapi\nf-imapi-iredbookdiscmaster-closeaudiotrack.md) | Closes a currently open audio track. All audio tracks must be closed before the IDiscMaster |
| [IRedbookDiscMaster::CreateAudioTrack](..\imapi\nf-imapi-iredbookdiscmaster-createaudiotrack.md) | Begins staging a new audio track. It can be called only when there are no open audio tracks in the image. |
| [IRedbookDiscMaster::GetAudioBlockSize](..\imapi\nf-imapi-iredbookdiscmaster-getaudioblocksize.md) | Retrieves the size, in bytes, of an audio block. |
| [IRedbookDiscMaster::GetAvailableAudioTrackBlocks](..\imapi\nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks.md) | Retrieves the current number of blocks that can be added to the track before an additional add will cause a failure for lack of space. |
| [IRedbookDiscMaster::GetTotalAudioBlocks](..\imapi\nf-imapi-iredbookdiscmaster-gettotalaudioblocks.md) | Retrieves the total number of blocks available for staging audio tracks. The total includes all block types, including blocks that may need to be allocated for track gaps. |
| [IRedbookDiscMaster::GetTotalAudioTracks](..\imapi\nf-imapi-iredbookdiscmaster-gettotalaudiotracks.md) | Retrieves the total number of tracks that have either been staged or are being staged. |
| [IRedbookDiscMaster::GetUsedAudioBlocks](..\imapi\nf-imapi-iredbookdiscmaster-getusedaudioblocks.md) | Retrieves the total number of audio blocks in use. |
| [IStreamConcatenate::Append2](..\imapi2\nf-imapi2-istreamconcatenate-append2.md) | Appends an array of streams to this stream. |
| [IStreamConcatenate::Append](..\imapi2\nf-imapi2-istreamconcatenate-append.md) | Appends a stream to this stream. |
| [IStreamConcatenate::Initialize2](..\imapi2\nf-imapi2-istreamconcatenate-initialize2.md) | Initializes this stream from an array of input streams. |
| [IStreamConcatenate::Initialize](..\imapi2\nf-imapi2-istreamconcatenate-initialize.md) | Initializes this stream from two input streams. |
| [IStreamInterleave::Initialize](..\imapi2\nf-imapi2-istreaminterleave-initialize.md) | Initialize this interleaved stream from an array of input streams and interleave sizes. |
| [IStreamPseudoRandomBased::get_ExtendedSeed](..\imapi2\nf-imapi2-istreampseudorandombased-get_extendedseed.md) | Retrieves an array of seed values used by the random number generator. |
| [IStreamPseudoRandomBased::get_Seed](..\imapi2\nf-imapi2-istreampseudorandombased-get_seed.md) | Retrieves the seed value used by the random number generator. |
| [IStreamPseudoRandomBased::put_ExtendedSeed](..\imapi2\nf-imapi2-istreampseudorandombased-put_extendedseed.md) | Sets a list of seed values for the random number generator and seeks to the start of stream. |
| [IStreamPseudoRandomBased::put_Seed](..\imapi2\nf-imapi2-istreampseudorandombased-put_seed.md) | Sets the seed value used by the random number generator and seeks to the start of stream. |
| [IWriteEngine2::CancelWrite](..\imapi2\nf-imapi2-iwriteengine2-cancelwrite.md) | Cancels a write operation that is in progress. |
| [IWriteEngine2::WriteSection](..\imapi2\nf-imapi2-iwriteengine2-writesection.md) | Writes a data stream to the current recorder. |
| [IWriteEngine2::get_BytesPerSector](..\imapi2\nf-imapi2-iwriteengine2-get_bytespersector.md) | Retrieves the number of bytes to use for each sector during writing. The returned value indicates what the value previously set with IWriteEngine2 |
| [IWriteEngine2::get_EndingSectorsPerSecond](..\imapi2\nf-imapi2-iwriteengine2-get_endingsectorspersecond.md) | Retrieves the estimated number of sectors per second that the recording device can write to the media at the end of the writing process. |
| [IWriteEngine2::get_Recorder](..\imapi2\nf-imapi2-iwriteengine2-get_recorder.md) | Retrieves the recording device to use in the write operation. |
| [IWriteEngine2::get_StartingSectorsPerSecond](..\imapi2\nf-imapi2-iwriteengine2-get_startingsectorspersecond.md) | Retrieves the estimated number of sectors per second that the recording device can write to the media at the start of the writing process. |
| [IWriteEngine2::get_UseStreamingWrite12](..\imapi2\nf-imapi2-iwriteengine2-get_usestreamingwrite12.md) | Retrieves a value that indicates if the write operations use the WRITE12 or WRITE10 command. |
| [IWriteEngine2::get_WriteInProgress](..\imapi2\nf-imapi2-iwriteengine2-get_writeinprogress.md) | Retrieves a value that indicates whether the recorder is currently writing data to the disc. |
| [IWriteEngine2::put_BytesPerSector](..\imapi2\nf-imapi2-iwriteengine2-put_bytespersector.md) | Sets the number of bytes to use for each sector during writing. |
| [IWriteEngine2::put_EndingSectorsPerSecond](..\imapi2\nf-imapi2-iwriteengine2-put_endingsectorspersecond.md) | Sets the estimated number of sectors per second that the recording device can write to the media at the end of the writing process. |
| [IWriteEngine2::put_Recorder](..\imapi2\nf-imapi2-iwriteengine2-put_recorder.md) | Sets a recording device for the write operation. |
| [IWriteEngine2::put_StartingSectorsPerSecond](..\imapi2\nf-imapi2-iwriteengine2-put_startingsectorspersecond.md) | Sets the estimated number of sectors per second that the recording device can write to the media at the start of the writing process. |
| [IWriteEngine2::put_UseStreamingWrite12](..\imapi2\nf-imapi2-iwriteengine2-put_usestreamingwrite12.md) | Sets a value that indicates if the write operations use the WRITE12 or WRITE10 command. |
| [IWriteEngine2EventArgs::get_FreeSystemBuffer](..\imapi2\nf-imapi2-iwriteengine2eventargs-get_freesystembuffer.md) | Retrieves the number of unused bytes in the internal data buffer that is used for writing to disc. |
| [IWriteEngine2EventArgs::get_LastReadLba](..\imapi2\nf-imapi2-iwriteengine2eventargs-get_lastreadlba.md) | Retrieves the address of the sector most recently read from the burn image. |
| [IWriteEngine2EventArgs::get_LastWrittenLba](..\imapi2\nf-imapi2-iwriteengine2eventargs-get_lastwrittenlba.md) | Retrieves the address of the sector most recently written to the device. |
| [IWriteEngine2EventArgs::get_SectorCount](..\imapi2\nf-imapi2-iwriteengine2eventargs-get_sectorcount.md) | Retrieves the number of sectors to write to the device in the current write operation. |
| [IWriteEngine2EventArgs::get_StartLba](..\imapi2\nf-imapi2-iwriteengine2eventargs-get_startlba.md) | Retrieves the starting logical block address (LBA) of the current write operation. |
| [IWriteEngine2EventArgs::get_TotalSystemBuffer](..\imapi2\nf-imapi2-iwriteengine2eventargs-get_totalsystembuffer.md) | Retrieves the size of the internal data buffer that is used for writing to disc. |
| [IWriteEngine2EventArgs::get_UsedSystemBuffer](..\imapi2\nf-imapi2-iwriteengine2eventargs-get_usedsystembuffer.md) | Retrieves the number of used bytes in the internal data buffer that is used for writing to disc. |
| [IWriteSpeedDescriptor::get_MediaType](..\imapi2\nf-imapi2-iwritespeeddescriptor-get_mediatype.md) | Retrieves type of media in the current drive. |
| [IWriteSpeedDescriptor::get_RotationTypeIsPureCAV](..\imapi2\nf-imapi2-iwritespeeddescriptor-get_rotationtypeispurecav.md) | Retrieves the supported rotational-speed control used by the recorder for the current media. |
| [IWriteSpeedDescriptor::get_WriteSpeed](..\imapi2\nf-imapi2-iwritespeeddescriptor-get_writespeed.md) | Retrieves the supported write speed for writing to the media. |
